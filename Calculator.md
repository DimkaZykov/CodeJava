# CodeJava
import java.util.*;

public class calculate {


    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String line = scanner.nextLine();
        var expression = line.split(" ");
        int fnum;
        int snum;
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
        if (roman.containsKey(expression[0])) {
            fnum = Integer.parseInt(roman.get(expression[0]));}
        else { fnum = Integer.parseInt(expression[0]);}
        if (roman.containsKey(expression[2])) {
            snum = Integer.parseInt(roman.get(expression[2]));}
        else { snum = Integer.parseInt(expression[2]);}

        switch (op) {
            case "+" -> System.out.println(fnum + snum);
            case "-" -> System.out.println(fnum - snum);
            case "/" -> System.out.println(fnum / snum);
            case "*" -> System.out.println(fnum * snum);
            default -> System.out.println("Введено необрабатываемое выражение");
        }

    }

}
