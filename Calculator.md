# CodeJava
import java.util.*;

public class calculate {


    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String line = scanner.nextLine();
        var expression = line.split(" ");
        if (expression.length < 3) {
            System.out.println("Нехватает значений");
        }
        int fnum = 0;
        int snum = 0;
        String op;
        op = expression[1];


        Map<String, String> roman = new HashMap<>();
        roman.put("I", "1");
        roman.put("II", "2");
        roman.put("III", "3");
        roman.put("IV", "4");
        roman.put("V", "5");
        roman.put("VI", "6");
        roman.put("VII", "7");
        roman.put("VIII", "8");
        roman.put("IX", "9");
        roman.put("X", "10");

        if (roman.containsKey(expression[0]) & roman.containsKey(expression[2])) {
            fnum = Integer.parseInt(roman.get(expression[0]));
            snum = Integer.parseInt(roman.get(expression[2]));
        }  if (!(roman.containsKey(expression[0])) & !(roman.containsKey(expression[2]))) {
            fnum = Integer.parseInt(expression[0]);
            snum = Integer.parseInt(expression[2]);
        } else {
            System.out.println("Введены числа разных типов");
        }

        switch (op) {
            case "+" -> System.out.println(fnum + snum);
            case "-" -> System.out.println(fnum - snum);
            case "/" -> System.out.println(fnum / snum);
            case "*" -> System.out.println(fnum * snum);
            default -> System.out.println("Введено необрабатываемое выражение");
        }

    }
}
