
import java.util.Date;

class Loan {
    private double annualInterestRate;
    private int numberOfYears;
    private double loanAmount;
    private Date loanDate;

    // Default constructor
    public Loan() {
        this(2.5, 1, 1000);
    }

    // Main constructor
    public Loan(double annualInterestRate, int numberOfYears, double loanAmount) {
        this.annualInterestRate = annualInterestRate;
        this.numberOfYears = numberOfYears;
        this.loanAmount = loanAmount;
        this.loanDate = new Date(); // Sets the date to the current time
    }

    // GETTERS
    public double getAnnualInterestRate() {
        return annualInterestRate;
    }


    public int getNumberOfYears() {
        return numberOfYears;

    }

    public double getLoanAmount() {
        return loanAmount;
    }

    public Date getLoanDate() {
        return loanDate;
    }

    //SETTERS (Fixed to accept parameters)
    public void setAnnualInterestRate(double annualInterestRate) {
        this.annualInterestRate = annualInterestRate;
    }

    public void setNumberOfYears(int numberOfYears) {
        this.numberOfYears = numberOfYears;
    }

    public void setLoanAmount(double loanAmount) {
        this.loanAmount = loanAmount;
    }

    // LOAN CALCULATIONS
    public double getMonthlyPayment() {
        double monthlyInterestRate = annualInterestRate / 1200;
        return loanAmount * monthlyInterestRate / (1 - (1 / Math.pow(1 + monthlyInterestRate, numberOfYears * 12)));
    }

    public double getTotalPayment() {
        return getMonthlyPayment() * numberOfYears * 12;
    }
}

public class Main {
    public static void main(String[] args) {


        Loan l1 = new Loan(5.5, 15, 250000);

        System.out.println("Loan Date: " + l1.getLoanDate());

        System.out.printf("Monthly Payment: %.2f\n", l1.getMonthlyPayment());

        System.out.printf("Total Payment: %.2f\n", l1.getTotalPayment());
    }
}


