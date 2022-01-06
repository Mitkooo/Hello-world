Exam exercise #1:


using System;

namespace Computer_Firm
{
    class Program
    {
        static void Main(string[] args)
        {
            int computersCount = int.Parse(Console.ReadLine());
            int ratingAndSales = 0;
            double salesCount = 0;
            double averageRating = 0;

            for (int i = 0; i < computersCount; i++)
            {
                ratingAndSales = int.Parse(Console.ReadLine());
                int currentRating = ratingAndSales % 10;
                int currentSales = ratingAndSales / 10;

                switch (currentRating)
                {
                    case 2:
                        salesCount += 0;
                        break;
                    case 3:
                        salesCount += currentSales * 0.50;
                        break;
                    case 4:
                        salesCount += currentSales * 0.70;
                        break;
                    case 5:
                        salesCount += currentSales * 0.85;
                        break;
                    case 6:
                        salesCount += currentSales;
                        break;
                }
                averageRating += currentRating; 
            }
            averageRating = averageRating / computersCount;
            Console.WriteLine($"{salesCount:F2}");
            Console.WriteLine($"{averageRating:F2}");
        }
    }
}

