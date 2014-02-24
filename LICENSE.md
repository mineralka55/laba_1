using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace melnikov_01
{
    class Program
    {
        static int A, B, C, D;
        static double  X= 0;
        static bool select;

        private static void Enter()
        {
            string n;
            Console.WriteLine("\nEnter A\n");
            n = (Console.ReadLine());
            while (!int.TryParse(n, out A))
            {
                Console.WriteLine("\nIncorrect input. Int type pls\n");
                n = Console.ReadLine();
            }
            Console.WriteLine("\nEnter B\n");
            n = (Console.ReadLine());
            while (!int.TryParse(n, out B))
            {
                Console.WriteLine("\nIncorrectr input. Int type pls\n");
                n = Console.ReadLine();
            }
            Console.WriteLine("\nEnter C\n");
            n = (Console.ReadLine());
            while (!int.TryParse(n, out C))
            {
                Console.WriteLine("\nIncorrect input. Int type pls\n");
                n = Console.ReadLine();
            }
            Console.WriteLine("\nEnter D\n");
            n = (Console.ReadLine());
            while (!int.TryParse(n, out D))
            {
                Console.WriteLine("\nIncorect input. Int type pls\n");
                n = Console.ReadLine();
            }
            Console.WriteLine("\nEnter X\n");
            n = (Console.ReadLine());
            while (!double.TryParse(n, out X))
            {
                Console.WriteLine("\nIncorrect input. Double type pls\n");
                n = Console.ReadLine();
            }
            Program.select = true;
        }
        private static void Сalculation()
        {
            if (Program.select == true)
            {
                Console.WriteLine("\n\n\nOtvet is : \n");
                Console.WriteLine((double)(A * (Math.Pow(X, 5)) + B * (Math.Pow(X, 3)) + (C * X) + (D / X)));
            }
            else
                Console.WriteLine("\nBefore calculate u need to enter variables\n");
        }
        private static void Main()
        {
            ConsoleKeyInfo key = new ConsoleKeyInfo();
            do
            {
                Console.WriteLine("\nThis program calculate :\n");
                Console.WriteLine("\nA * X^5 + B * X^3 + C * X + (D div E)\n");
                Console.WriteLine("\nA,B,C,D are integer\n");
                Console.WriteLine("\nX is double\n");
                Console.WriteLine("1. Input values\n");
                Console.WriteLine("2. Otvet\n");
                Console.WriteLine("3. Exit\n");
                key = Console.ReadKey();
                if (key.KeyChar == '1')
                    Enter();
                if (key.KeyChar == '2')
                    Сalculation();
                if (key.KeyChar == '3')
                    break;
            }
            while (key.KeyChar != '3');
        }

    }
}

