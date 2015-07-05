# Dibujo-de-Array
Ingresamos un array y el programa nos dibuja una grafica del array
package PackOne;

public class Numeral {

    public static void main(String[] args) {
//        int[] input = {5, 7, 8, 3, 2, 11, 10};
//        int[] input = {9,2,6,5,6,2,1};
        int[] input = {15,18,20,4,7,8,1,6};
        print(input);
    }
    public static void print(int[] input) {
        int n = 1;
        for (int i = 0; i < input.length; i++) {
            if (input[i] > n) {
                n = input[i];
            }
        }
        int count = n;

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < input.length; j++) {
              if(count <= input[j]){
                  System.out.print("# ");
              }else{System.out.print("  ");}
            }
            --count;
            System.out.println();
        }
        
        for (int i = 0; i < input.length; i++) {
            System.out.print("- ");
        }
        System.out.println();
        for (int i = 1; i <= input.length; i++) {
            System.out.print(i+" ");
        }
        System.out.println();
    }
}
