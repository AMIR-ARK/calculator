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
            Console.Write("adad aval ra vared konid: ");
            num1 = double.Parse(Console.ReadLine());

            Console.Write("adad dovom ra vared konid: ");
            num2 = double.Parse(Console.ReadLine());

            Console.Write("mohasebe khod ra entekhab konid  (+, -, *, /) ya q ra bray kharej shodan deshar dahid: ");
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
                        Console.WriteLine("Error: taghsim bar sefr");
                    }
                    else
                    {
                        result = num1 / num2;
                        Console.WriteLine("{0} / {1} = {2}", num1, num2, result);
                    }
                    break;
                case 'q':
                    Console.WriteLine("dar hal khoroj...");
                    exit = true;
                    break;
                default:
                    Console.WriteLine("amaliat na morabar!");
                    break;
            }

            Console.WriteLine();
        }
    }
}
