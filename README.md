# Projects_

import java.util.Scanner;

public class Banking_System_02
{
    static int balance=0;

    public static void main(String[] args) {
    Scanner sc=new Scanner(System.in);

    int option=0;
        while(option!=4) {

            System.out.println("_______________WELCOME TO THE BANK OF MONEY__________");
            System.out.println("PRESS 1. CHECK BALANCE");
            System.out.println("PRESS 2. DEPOSIT");
            System.out.println("PRESS 3. WITHDRAW");
            System.out.println("PRESS 4. EXIT");
            System.out.println("SELECT ANY OPTION");
            option=sc.nextInt();

            switch (option){
                case 1:
                    checkBalance();
                    break;

                case 2:
                    Deposite();
                    break;

                case 3:
                    Withdraw();
                    break;

                case 4:
                    Exit();
                    break;

                default:
                    System.out.println("Invalid Option");
            }
            }
    }


     public static void checkBalance() {
         System.out.println("YOUR CURRENT BALANCE IS:" + balance);

     }
     public static void Deposite() {
        Scanner sc=new Scanner(System.in);
         System.out.println("ENTER THE AMOUNT TO DEPOSITE");
        int amount=sc.nextInt();
        balance+=amount;
         System.out.println(amount+" HAS BEEN DEPOSITED TO YOUR ACCOUNT");

         System.out.println("NOW TOTAL BALANCE IS:");
         checkBalance();
    }
    public static void Withdraw(){
        Scanner sc=new Scanner(System.in);
        System.out.println("ENTER THE AMOUNT TO WITHDRAW");
        int amount=sc.nextInt();
        if(amount > balance){
            System.out.println("xxxxxxINSUFFICIENT FUNDxxxxxxx");

        }
        else{
            balance-=amount;
        }

        System.out.println("YOUR TOTAL BALANCE IS:");
        checkBalance();

    }

    public static void Exit(){
        System.out.println("THANK YOU FOR USING OUR SERVICE. HAVE NICE DAY");
    }


    }




