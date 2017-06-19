using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Point_on_Segment
{
    class Program
    {
        static void Main(string[] args)
        {
            int first = int.Parse(Console.ReadLine());
            int second = int.Parse(Console.ReadLine());
            int point = int.Parse(Console.ReadLine());
            if (first < second)
            {
                if (point >= first && point <= second)
                {
                    int fSide = (point - first);
                    int sSide =Math.Abs(second - point);

                    Console.WriteLine("in");

                    if (fSide >= sSide)
                    {
                        Console.WriteLine(sSide);
                    }
                    else
                    {
                        Console.WriteLine(fSide);
                    }

                }
                else
                {
                    Console.WriteLine("out");
                    if (point < first)
                    {
                        int fSide =Math.Abs(first - point);
                        Console.WriteLine(fSide);
                    }
                    else
                    {
                        int sSide =Math.Abs(point - second);
                        Console.WriteLine(sSide);
                    }
                }
            }
            else
            {
                if (point <= first && point >= second)
                {
                    int fSide =Math.Abs(first - point);
                    int sSide =Math.Abs(point - second);

                    Console.WriteLine("in");

                    if (fSide >= sSide)
                    {
                        Console.WriteLine(sSide);
                    }
                    else
                    {
                        Console.WriteLine(fSide);
                    }

                }
                else
                {
                    Console.WriteLine("out");
                    if (point > first)
                    {
                        int fSide =Math.Abs(first - point);
                        Console.WriteLine(fSide);
                    }
                    else
                    {
                        int sSide =Math.Abs(point - second);
                        Console.WriteLine(sSide);
                    }
                }
            }
        }
    }
}
