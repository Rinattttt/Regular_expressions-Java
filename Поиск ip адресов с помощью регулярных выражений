import java.io.FileWriter;
import java.io.IOException;
import java.util.regex.Matcher;
import java.util.regex.Pattern;
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        System.out.println("Введите проверяемую строку: ");
        Scanner input = new Scanner(System.in);
        String STR = input.nextLine();
        String reg = "[0-9a-fA-F]{1,4}";
        String ipv6 = "(" + reg + ":){7}" + reg + "|(" + reg + ":){1,7}:|" + "(" + reg + ":){1,6}" + reg + "|" + "(" + reg + ":){1,5}(" + reg + ":){1,2}|" + "(" + reg + ":){1,4}(" + reg + ":){1,3}|" + "(" + reg + ":){1,3}(" + reg + ":){1,4}|" + "(" + reg + ":){1,2}(" + reg + ":){1,5}|" + reg + ":(:" + reg + "{1,4}){1,6}|" + ":((:" + reg + "){1,7}|:)";
        String ipv4 = "(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)";
        Pattern patternv6 = Pattern.compile(ipv6);
        Pattern patternv4 = Pattern.compile(ipv4);
        Matcher matcher6 = patternv6.matcher(STR);
        Matcher matcher4 = patternv4.matcher(STR);
        int a = 0;
        try {
            FileWriter file = new FileWriter("C:\\Users\\kosoi\\IdeaProjects\\input.txt");
            while (matcher6.find()) {
                file.write("Найденный IPV6-адрес: " + matcher6.group(0));
                a++;
            }
            while (matcher4.find()) {
                file.write("Найденный IPV4-адрес: " + matcher4.group(0));
                a++;
            }
            file.close();
        }
        catch
        (IOException ex) {
            System.out.println(ex.getMessage());
        }
        if(a<1){
            System.out.println("Ни один из адресов не найден.");
        }
    }
}

