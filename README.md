# Suffix-Array
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.IO;

namespace SA2
{
    class Program
    {
        static void Main(string[] args)
        {
            StreamReader str = new StreamReader("C:\\Users\\Amsal\\Desktop\\TextFile1.txt");
            string name = str.ReadLine();
            Console.WriteLine("Taking input from the file:\t{0}\n-----------------------------------------", name);
            int n = name.Length;
            Console.WriteLine("\n-----------------------------------------\nAfter Making Substrings\n-----------------------------------------\n");
            string[] arr = new string[name.Length];

            string s = name;
            for (int i = 0; i < name.Length + i; i++)
            {
                arr[i] = name;
                name = name.Substring(1);
                Console.WriteLine(arr[i]);
            }
            Console.WriteLine("\n-----------------------------------------\nThe Sorted List of strings\n-----------------------------------------\n");
            Array.Sort(arr, StringComparer.InvariantCulture);

            for (int j = 0; j < n; j++)
            {

                Console.WriteLine(arr[j]);
            }
            Console.ReadLine();


        }
    }
}
