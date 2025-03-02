# Array5
Sort the Array having 0s and 1s only

// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        int count = 0;
        System.out.println("Enter the size of the Array");
        Scanner sc = new Scanner(System.in);
        int size=sc.nextInt();
         System.out.println("Enter the Numbers in the Array");
        int[] binaryNum = new int[size];
        for(int i=0;i<binaryNum.length;i++){
            binaryNum[i]=sc.nextInt();
        }
        System.out.println("Entered array is");
        for(int l=0;l<binaryNum.length;l++){
            System.out.print(binaryNum[l]);
        }
        System.out.println();
        for(int i=0;i<binaryNum.length;i++){
            if(binaryNum[i]==0){
                count++;
            }
            else{
                continue;
            }
        }
        for(int j=0;j<count;j++){
            binaryNum[j]=0;
        }
        for(int k=count;k<binaryNum.length;k++){
            binaryNum[k]=1;
        }
        System.out.println("Sorted array is");
        for(int l=0;l<binaryNum.length;l++){
            System.out.print(binaryNum[l]);
        }
    }
}

Enter the size of the Array
9
Enter the Numbers in the Array
1 0 0 1 0 1 1 0 0
Entered array is
100101100
Sorted array is
000001111
=== Code Execution Successful ===

2. Sort the Array having only 0s and 1s with two pointer method (Two poiter method)

// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.Scanner;
class Main {
    static void swap(int arr[], int i, int j){
        int temp=arr[i];
        arr[i]=arr[j];
        arr[j]=temp;
    }
    
    static void printArray(int arr[]){
        int n= arr.length;
        System.out.println("The entered array elements are");
        for(int i=0;i<n;i++){
            System.out.print(arr[i]+" ");
        }
        System.out.println();
    }
    static void inputArray(int arr[], int size,Scanner sc){
        System.out.println("Enter the Array elements");
        for(int i=0;i<size;i++){
            arr[i] = sc.nextInt();
        }
    }
    static void sortZeroesandOnes(int arr[]){
        int n= arr.length;
        System.out.println("Sorting the Array");
        int left = 0, right=n-1;
        
        while(left<right){
            if(arr[left] == 1 && arr[right]==0){
                swap(arr,left,right);
                left++;
                right--;
            }
            if(arr[left]==0){
                left++;
            }
            if(arr[right]==1){
                right--;
            }
        }
    }
    public static void main(String[] args) {
        System.out.println("Try programiz.pro");
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the Size of the Array");
        int size = sc.nextInt();
        int[] binArray = new int[size];
        inputArray(binArray,size,sc);
        printArray(binArray);
        sortZeroesandOnes(binArray);
        printArray(binArray);
    }
}

Try programiz.pro
Enter the Size of the Array
8
Enter the Array elements
1 0 1 0 1 0 1 0
The entered array elements are
1 0 1 0 1 0 1 0 
Sorting the Array
The entered array elements are
0 0 0 0 1 1 1 1 

=== Code Execution Successful ===

3.Given an Array a , move all the even integers towards the Start of the Array and followed by the odd integers , the relative order of the two parts doesnt,t matter, return whichever code that satisfies this condition

// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.Scanner;
class Main {
    static void swap(int arr[], int i, int j){
        int temp=arr[i];
        arr[i]=arr[j];
        arr[j]=temp;
    }
    
    static void printArray(int arr[]){
        int n= arr.length;
        System.out.println("The entered array elements are");
        for(int i=0;i<n;i++){
            System.out.print(arr[i]+" ");
        }
        System.out.println();
    }
    static void inputArray(int arr[], int size,Scanner sc){
        System.out.println("Enter the Array elements");
        for(int i=0;i<size;i++){
            arr[i] = sc.nextInt();
        }
    }
    static void sortArrayByParity(int arr[]){
        int n= arr.length;
        System.out.println("Sorting the Array");
        int left = 0, right=n-1;
        
        while(left<right){
            if(arr[left] % 2== 1 && arr[right] % 2==0){
                swap(arr,left,right);
                left++;
                right--;
            }
            if(arr[left] % 2 ==0){
                left++;
            }
            if(arr[right] % 2 ==1){
                right--;
            }
        }
    }
    public static void main(String[] args) {
        System.out.println("Try programiz.pro");
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the Size of the Array");
        int size = sc.nextInt();
        int[] binArray = new int[size];
        inputArray(binArray,size,sc);
        printArray(binArray);
        sortArrayByParity(binArray);
        printArray(binArray);
    }
}

Try programiz.pro
Enter the Size of the Array
8
Enter the Array elements
1 3 6 8 62 8 7 9
The entered array elements are
1 3 6 8 62 8 7 9 
Sorting the Array
The entered array elements are
8 62 6 8 3 1 7 9 

=== Code Execution Successful ===

4. Given An array which is sorted in non-decreasing order, return the square of each element in the non-decreasing order,

// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.Scanner;
class Main {
    static void swap(int arr[],int i, int j){
        int temp = arr[i];
        arr[i]=arr[j];
        arr[j]=temp;
    }
    
  static void printArray(int arr[]){
        int n= arr.length;
        System.out.println("The entered array elements are");
        for(int i=0;i<n;i++){
            System.out.print(arr[i]+" ");
        }
        System.out.println();
    }
    static void inputArray(int arr[], int size,Scanner sc){
        System.out.println("Enter the Array elements");
        for(int i=0;i<size;i++){
            arr[i] = sc.nextInt();
        }
    }
    static void returnSquare(int arr[]){
        int n = arr.length;
        for(int i=0;i<n;i++){
            arr[i] = arr[i] * arr[i];
        }
    }
    static void SortArray(int arr[]){
        int n = arr.length;
        for(int i=0;i<n-1;i++){
            for(int j=i+1;j<n;j++){
                if(arr[i] > arr[j]){
                    swap(arr,i,j);
                }
            }
        }
    }
    
    
    public static void main(String[] args) {
        System.out.println("Try programiz.pro");
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the Size of the Array");
        int size = sc.nextInt();
        int[] binArray = new int[size];
        inputArray(binArray,size,sc);
        printArray(binArray);
        returnSquare(binArray);
        SortArray(binArray);
        printArray(binArray);
    }
}

Try programiz.pro
Enter the Size of the Array
6
Enter the Array elements
-10 -3 -2 1 4 5 
The entered array elements are
-10 -3 -2 1 4 5 
The entered array elements are
1 4 9 16 25 100 

=== Code Execution Successful ===



