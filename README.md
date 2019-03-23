# Journey

import  java.util.Scanner;

public class P40_Journey {

    public static void main(String[] args) {
        Scanner console = new Scanner(System.in);
        double budget = Double.parseDouble(console.nextLine());
        String season = console.nextLine();

        String destination = "";
        double expendMoney = 0;
        String place = "";

        if (budget <= 100){
            destination = "Bulgaria";
            if (season.equalsIgnoreCase("summer")){
                expendMoney = 0.30 * budget;
                place = "Camp";
            } else if (season.equalsIgnoreCase("winter")){
                expendMoney = 0.70 * budget;
                place = "Hotel";
            } else {
                System.out.print("error");
            }
        } else if (budget <= 1000){
            destination = "Balkans";
            if (season.equalsIgnoreCase("summer")){
                expendMoney = 0.40 * budget;
                place = "Camp";
            } else if (season.equalsIgnoreCase("winter")){
                expendMoney = 0.80 * budget;
                place = "Hotel";
            } else {
                System.out.print("error");
            }
        } else {
            destination = "Europe";
            place = "Hotel";
            expendMoney = 0.9 * budget;
        }
        System.out.printf("Somewhere in %s\n", destination);
        System.out.printf("%s - %.2f", place, expendMoney);
    }

}
