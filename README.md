# Answer-to-the-test
//testsolution

import java.util.Scanner;

public class Spiral_matrix {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		 Scanner s = new Scanner(System.in);
         System.out.print("Enter the number of elements : ");
         int n = s.nextInt();

         int A[][] = new int[n][n];
         int a=1, c1=0, c2=n-1, r1=0, r2=n-1;

         while(a<=n*n)
             {
                 for(int i=c1;i<=c2;i++)
                 {
                     A[r1][i]=a++;
                 }

                 for(int j=r1+1;j<=r2;j++)
                 {
                     A[j][c2]=a++;
                 }

                 for(int i=c2-1;i>=c1;i--)
                 {
                     A[r2][i]=a++;
                 }

                 for(int j=r2-1;j>=r1+1;j--)
                 {
                     A[j][c1]=a++;
                 }

              c1++;
              c2--;
              r1++;
              r2--;
             }
         System.out.println("The Circular Matrix is:");
         for(int i=0;i<n;i++)
             {
                 for(int j=0;j<n;j++)
                     {
                         System.out.print(A[i][j]+ "\t");
                     }
              System.out.println();
             }

	}

}
