using System;

class Program
{
    static void Main()
    {
        // Display the welcome message to the user
        Console.WriteLine("Welcome to Package Express. Please follow the instructions below.");

        // Ask the user to enter the package weight
        Console.WriteLine("Please enter the package weight:");

        // Read the user's input and convert it into a decimal number
        decimal weight = Convert.ToDecimal(Console.ReadLine());

        // Check if the package weight is greater than 50
        if (weight > 50)
        {
            // Show an error message if the package is too heavy
            Console.WriteLine("Package too heavy to be shipped via Package Express. Have a good day.");

            // End the program
            return;
        }

        // Ask the user to enter the package width
        Console.WriteLine("Please enter the package width:");

        // Read the width entered by the user
        decimal width = Convert.ToDecimal(Console.ReadLine());

        // Ask the user to enter the package height
        Console.WriteLine("Please enter the package height:");

        // Read the height entered by the user
        decimal height = Convert.ToDecimal(Console.ReadLine());

        // Ask the user to enter the package length
        Console.WriteLine("Please enter the package length:");

        // Read the length entered by the user
        decimal length = Convert.ToDecimal(Console.ReadLine());

        // Check if the total dimensions are greater than 50
        if (width + height + length > 50)
        {
            // Show an error message if the package is too large
            Console.WriteLine("Package too big to be shipped via Package Express.");

            // End the program
            return;
        }

        // Calculate the shipping quote using the required formula
        decimal quote = (width * height * length * weight) / 100;

        // Display the final quote as a dollar amount with 2 decimal places
        Console.WriteLine("Your estimated total for shipping this package is: $" + quote.ToString("F2"));

        // Thank the user at the end
        Console.WriteLine("Thank you!");
    }
}