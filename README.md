# HW4-
namespace Homework4_1
    {
        class Program
        {
            static void Main(string[] args)
            {
                string name1 = GetFullName();
                Console.WriteLine(name1);
            //string name2 = GetFullName();
            //Console.WriteLine(name2);
            //string name3 = GetFullName();
            //Console.WriteLine(name3);
            Console.ReadLine();
            }
            static string GetFullName()
            {
                string firstName = Console.ReadLine();
                string patronymic = Console.ReadLine();
                string lastName = Console.ReadLine();
                string fullName = ($" {firstName} ; {patronymic} ;  {lastName} ");

                return fullName;
            }
        }
    }

namespace HW4_3
{
    class Program
    {
        enum Season
        {
            Spring,
            Summer,
            Autumn,
            Winter
        }
        static void Main(string[] args)
        {
            Console.WriteLine("Введите номер месяца");
            int numOfMonth = Convert.ToInt32(Console.ReadLine());
            if(numOfMonth==12||numOfMonth==1||numOfMonth==2)
                Console.WriteLine("Время года - зима");
            else if(numOfMonth==3||numOfMonth==4||numOfMonth==5)
                Console.WriteLine("Время года - весна");
            else if (numOfMonth == 6 || numOfMonth == 7 || numOfMonth == 8)
                Console.WriteLine("Время года - лето");
            else if (numOfMonth == 9 || numOfMonth == 10 || numOfMonth == 11)
                Console.WriteLine("Время года - осень");
            else
                Console.WriteLine("Ошибка: введите число от 1 до 12");
            Console.ReadLine();
        }
    }
}

namespace HW4_2
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите набор чисел через пробел:\t");
            string setOfNumbersThanSpace = Console.ReadLine();
            string[] setOfNumbers = setOfNumbersThanSpace.Split(' ');  //Из строки удалим пробел
            int[] arrayNumbers = Convert.ToInt32(setOfNumbers());//выдает ошибку: "не удается неявно преобразовать тип "int" в "int[]".

            for (int i = 0; i < arrayNumbers.Length; i++) //цикл ввожу для проверки удаления пробела
            {
                Console.Write(arrayNumbers[i]);
            }
            
            int sum = arrayNumbers.Sum(); //в виду ошибки в предыдущей строке не удается проверить код в этой строке
            Console.Write("Сумма всех чисел в строке равна: " + sum);
            Console.ReadLine();

        }
    }
}
