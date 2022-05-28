# Operator-Overloading

## Aim:
 To write a C# program to find the volume of a box using operator overloading
 
 ## Algorithm:
 ### Step1:
Create a class for operator overloading.
### Step2:
Get inputs for length,breadthandheight of the box from the user and then calculate the volume in overloading function.
### Step3:
After that return a new object for the calculated volume.
### Step4:
Then create a new object to store the return object.
### Step5:
After that print the calculated volume.
 
 
 ## Program:
 ```c#
 using System;
class example
{
    public int length, breadth, height, volume;
    public static example operator +(example e1, example e2)
    {
        example e3 = new example();
        e1.volume = e1.length * e1.height * e1.breadth;
        e2.volume = e2.length * e2.height * e2.breadth;
        e3.length = e1.length + e2.length;
        e3.breadth = e1.breadth + e2.breadth;
        e3.height = e1.height + e2.height;
        e3.volume = e3.length * e3.breadth * e3.height;
        return e3;
    }
    public static void Main()
    {
        example[] e = new example[2];
        e[0] = new example();
        e[1] = new example();

        for (int i = 0; i < 2; i++)
        {
            Console.WriteLine("Enter lenght of Box {0}", i + 1);
            e[i].length = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter breadth of Box {0}", i + 1);
            e[i].breadth = Convert.ToInt32(Console.ReadLine()); ;
            Console.WriteLine("Enter height of Box {0}", i + 1);
            e[i].height = Convert.ToInt32(Console.ReadLine()); ;
        }
        example e3 = new example();
        e3 = e[0] + e[1];
        Console.WriteLine("Volume of Box 1 is {0}\nVolume of Box 2 is {1}\nVolume of Box 3 is {2}", e[0].volume, e[1].volume, e3.volume);
    }
}
 ```
 
 ## Output:
 ![image](https://user-images.githubusercontent.com/75235488/170663961-470b3e73-2411-4da8-8f21-5bfd3ac1abf4.png)

 
 ## Result:
C# program to find the volume of a box using operator overloading is implemented successfully.
