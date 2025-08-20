# 🔌 SmartDevice Power Simulation

A simple Java program to **simulate power consumption** of electronic devices.  
It takes the **power rating (Watts)** and **usage time (hours)** as input, and calculates the total energy consumed in **kilowatt-hours (kWh)**.

---

## ✨ Features
- Input device **power rating in Watts**.
- Input **usage duration in hours**.
- Calculates energy consumption with the formula:

  \[
  \text{Energy (kWh)} = \frac{\text{Power Rating (W)} \times \text{Usage Hours (h)}}{1000}
  \]

- Displays a clean summary of results.

---

## 📄 Source Code

```java
import java.util.Scanner;

public class SmartDevicePowerSimulation {

    // Method to calculate energy consumption in kWh
    public static double simulatePowerConsumption(double powerRatingWatts, double usageHours) {
        return (powerRatingWatts * usageHours) / 1000;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter power rating of device (in Watts): ");
        double powerRatingWatts = sc.nextDouble();

        System.out.print("Enter usage time (in hours): ");
        double usageHours = sc.nextDouble();

        double consumption = simulatePowerConsumption(powerRatingWatts, usageHours);

        System.out.println("\nPower Rating: " + powerRatingWatts + " Watts");
        System.out.println("Usage Time: " + usageHours + " hours");
        System.out.println("Power Consumption: " + consumption + " kWh");

        sc.close();
    }
}
