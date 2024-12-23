package Sesi_12;

    public class No_1 {
    public static void reverse(int n) {

    for (int i = n; i >= 1; i--) {
        System.out.print(i);
        if (i > 1) System.out.print(",");
    }
    System.out.println();
    { public static void main(String[] args) {
    reverse(7);
    }
}


package Sesi_12;

    import java.util.Scanner;

    public class No_2 {
    
    public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);
    System.out.print("Masukkan kata atau kalimat: ");
    String input = scanner.nextLine();
    scanner.close();
    if (isPalindrom(input)) {
        System.out.println("'"+input + "' adalah palindrom.");
    } else {
        System.out.println("'"+input + "' bukan palindrom.");
    }
    } public static boolean isPalindrom(String str) {
    str = str.replaceAll("\\s", "").toLowerCase(); 
    int start = 0;
    int end = str.length() - 1;
    while (start < end) {
        if (str.charAt(start) != str.charAt(end)) {
            return false;
        }
        start++;
        end--;
    }
    return true;
}
}


package Sesi_12; 

    public class No_3 {

    public static boolean contains(int[] 
    arr, int n, int target) {

    if (n == arr.length) {
        return false;
    } else if (arr[n] == target) {
        return true;
    }
    return contains(arr, n + 1, target);
     } public static void main(String[] args) {
    int arr[] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    int target = 12;
    boolean result = contains(arr, 0, target);
    System.out.println("Target ada di dalam array: " + result);
    }
}


package Sesi_12;

    public class No_4 {

    public static int findMax(int[] arr, int n) {
        if (n == 1) {
            return arr[0];
        } else {
            int max = findMax(arr, n - 1);
            return (arr[n - 1] > max) ? arr[n - 1] : max;
        }
    }
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 7, 5};
        int n = arr.length;
        System.out.println("Nilai maksimum: " + findMax(arr, n));
    }
}  

package Sesi_12;

    public class No_5 {

    public static int sumOfThree(int n, int a, int b, int c ) {
    if (n==0) {
        return 0;
    }else {
        System.out.print(a+",");
        sumOfThree(n-1, b, c, a+b+c);
    }
    return 0;
    }
    public static void main(String[] args){
    int n = 5;
    int a =1;
    int b =1;
    int c=1;
    sumOfThree(n, a, b, c);
    }
 }
