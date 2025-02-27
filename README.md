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
