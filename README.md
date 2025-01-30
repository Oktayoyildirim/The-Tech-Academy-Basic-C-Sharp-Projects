# The-Tech-Academy-Basic-C-Sharp-Projects
repository to store your coding projects from this course
using System;

class Program
{
    static void Main()
    {
        // Display the initial welcome message to the user.
        Console.WriteLine("Welcome to Package Express. Please follow the instructions below.");

        // Prompt the user to enter the package weight.
        Console.WriteLine("Please enter the package weight:");
        double weight = Convert.ToDouble(Console.ReadLine()); // Get the weight input from the user and convert it to double.

        // Check if the weight is greater than 50 and display an error message if true.
        if (weight > 50)
        {
            Console.WriteLine("Package too heavy to be shipped via Package Express. Have a good day.");
            return; // End the program if the weight is too heavy.
        }

        // Prompt the user to enter the package width.
        Console.WriteLine("Please enter the package width:");
        double width = Convert.ToDouble(Console.ReadLine()); // Get the width input and convert it to double.

        // Prompt the user to enter the package height.
        Console.WriteLine("Please enter the package height:");
        double height = Convert.ToDouble(Console.ReadLine()); // Get the height input and convert it to double.

        // Prompt the user to enter the package length.
        Console.WriteLine("Please enter the package length:");
        double length = Convert.ToDouble(Console.ReadLine()); // Get the length input and convert it to double.

        // Check if the total dimensions (width + height + length) are greater than 50 and display an error message if true.
        if (width + height + length > 50)
        {
            Console.WriteLine("Package too big to be shipped via Package Express.");
            return; // End the program if the package is too big.
        }

        // Multiply the width, height, and length to get the volume, and multiply it by the weight.
        double quote = (width * height * length * weight) / 100; // Calculate the quote by dividing the product by 100.

        // Display the final shipping quote to the user.
        Console.WriteLine($"Your estimated total for shipping this package is: ${quote:F2}");

        // Thank the user for using Package Express.
        Console.WriteLine("Thank you!");
    }
}
