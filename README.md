import java.util.Scanner;

public class Main {

    static int totalMarks(int[] marks) {
        int sum = 0;

        for(int i = 0; i < marks.length; i++) {
            sum = sum + marks[i];
        }

        return sum;
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter Name: ");
        String name = sc.next();

        int[] marks = new int[3];

        System.out.println("Enter 3 Marks:");

        for(int i = 0; i < 3; i++) {
            marks[i] = sc.nextInt();
        }

        int total = totalMarks(marks);

        System.out.println("Total Marks: " + total);

        if(total >= 150) {
            System.out.println(name + " Passed");
        } else {
            System.out.println(name + " Failed");
        }
    }
}
