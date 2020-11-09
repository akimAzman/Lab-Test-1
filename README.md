# Lab-Test-1

     class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Input an Integer to count Set Bits:");
            System.Console.WriteLine($"Result: {CountSetBits(Convert.ToInt32(args[0]))}");
        }

        public static int CountSetBits(int n)
        {
            var count = 0;
            if (n == 0)
            {
                return count;
            }
            else
            {
                var binary = Convert.ToString(n, 2);
                System.Console.WriteLine($"Binary Representation: {binary}");
                //Non Recursive Method
                // foreach (var bit in binary.ToCharArray())
                // {
                //     if (bit == '1')
                //     {
                //         count++;
                //     }
                // }
                // return count;
                return CountSetBitsUtil(n);
            }
        }

        public static int CountSetBitsUtil(int n)
        {
            if (n <= 0)
                return 0;
            else
            {
                return (n % 2 == 0 ? 0 : 1) + CountSetBitsUtil(n / 2);
            }
        }
    }
}
