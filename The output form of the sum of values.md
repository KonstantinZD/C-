using System;
using System.Linq;
using System.Text.RegularExpressions;
 
public class Example
{
    public static void Main()
    {
        string input = @"11.12.1996";
        
        Console.WriteLine(Regex.Matches(input, @"\d").Cast<Match>().Sum(x => int.Parse(x.Value))); //1
        
        Console.WriteLine(input.Where(char.IsDigit).Sum(x => x -'0')); //2
    }
}
