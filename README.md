# calculator c# tamrin
using System;

class Calculator
{
    static void Main()
    {
        double num1, num2, result;
        char op;
        bool exit = false;

        Console.WriteLine("Simple Calculator\n");

        while (!exit)
        {
            Console.Write("Enter first number: ");
            num1 = double.Parse(Console.ReadLine());

            Console.Write("Enter second number: ");
            num2 = double.Parse(Console.ReadLine());

            Console.Write("Enter an operator (+, -, *, /) or q to quit: ");
            op = char.Parse(Console.ReadLine());

            switch (op)
            {
                case '+':
                    result = num1 + num2;
                    Console.WriteLine("{0} + {1} = {2}", num1, num2, result);
                    break;
                case '-':
                    result = num1 - num2;
                    Console.WriteLine("{0} - {1} = {2}", num1, num2, result);
                    break;
                case '*':
                    result = num1 * num2;
                    Console.WriteLine("{0} * {1} = {2}", num1, num2, result);
                    break;
                case '/':
                    if (num2 == 0)
                    {
                        Console.WriteLine("Error: division by zero");
                    }
                    else
                    {
                        result = num1 / num2;
                        Console.WriteLine("{0} / {1} = {2}", num1, num2, result);
                    }
                    break;
                case 'q':
                    Console.WriteLine("Exiting...");
                    exit = true;
                    break;
                default:
                    Console.WriteLine("Invalid operator!");
                    break;
            }

            Console.WriteLine();
        }
    }
}
