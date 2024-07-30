import java.util.Scanner;

class Variable {
    int a,b;
    char sign;

    Variable(int aa, int bb, char c){
        a = aa;
        b = bb;
        sign = c;
    }
    int addition(){
        return a+b;
    }
    int subtraction(){
        return a-b;
    }
    int multiplication(){
        return a*b;
    }
    int divide(){
        return a/b;
    }
}
public class calculator {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        System.out.println("Enter first value: ");
        int aa = sc.nextInt();
        System.out.println("Enter second value: ");
        int bb = sc.nextInt();
        System.out.println("Enter sign: ");
        char c = sc.next().charAt(0);
        
        Variable var1 = new Variable(aa, bb, c);
        Variable var2 = new Variable(aa, bb, c);
        Variable var3 = new Variable(aa, bb, c);
        Variable var4 = new Variable(aa, bb, c);
        
        switch(c){
            case '+' : System.out.println("Result: " + var1.addition());
            break;

            case '-' : System.out.println("Result: " + var2.subtraction());
            break;

            case '*' : System.out.println("Result:" + var3.multiplication());
            break;

            case '/' : System.out.println("Result: " + var4.divide());
            break;

            default: System.out.println("Invalid Input!!");
            break;
        }
    }
}
