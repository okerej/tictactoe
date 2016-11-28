# tictactoe
#just a basic tic tac toe game i wrote in c#
#
#this tic tac toe game only runs once. I just wanted to see if i could create it. the code is below.
#feel free to test. At the time of this upload I am very new to Github.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
/*
 * 
 * This is a small Tic Tac Toe program. This program can be improved dramatically, but
 * for now, it does the job.
 * 
 */

namespace TicTacToe
{
    class Program
    {

        static void Main(string[] args)
        {
            string[,] xoArray = new string[3, 3];
            string[] letters = new string[] { "a", "b", "c", "d", "e", "f", "g", "h", "i" };
            string xoLetter = "X";
            string xoOption;
            bool xoBool = false;
            int i = 0;

            while (i < 9)
            {
                for (int j = 0; j < 3; j++)
                {
                    for (int k = 0; k < 3; k++)
                    {
                        xoArray[j, k] = letters[i];
                        i++;
                    }
                }                
            }

            
            Console.WriteLine("This is a Tic Tac Toe Game...");
            Console.WriteLine("Press Enter to play the game");
            Console.ReadKey();
            Console.Clear();
                        
            int z = 0;
            while (z < 9 )  
            {
                Console.WriteLine(" [" + xoArray[0, 0] + "][" + xoArray[0, 1] + "][" + xoArray[0, 2] + "]");
                Console.WriteLine(" [" + xoArray[1, 0] + "][" + xoArray[1, 1] + "][" + xoArray[1, 2] + "]");
                Console.WriteLine(" [" + xoArray[2, 0] + "][" + xoArray[2, 1] + "][" + xoArray[2, 2] + "]");
                Console.WriteLine("Enter a letter from a through i for where you want X or O to be displayed");
                
                while (xoBool == false)
                {
                    xoOption = Console.ReadLine();
                    switch (xoOption)
                    {
                        case "a":
                            if ((xoArray[0, 0] == "X") || (xoArray[0, 0] == "O"))
                            {
                                Console.WriteLine("'a' is already chosen.");
                                break;
                            }
                            else
                            {
                                xoArray[0, 0] = xoLetter;
                                z++;
                                xoBool = true;
                                break;
                            }
                        case "b":
                            if ((xoArray[0, 1] == "X") || (xoArray[0, 1] == "O"))
                            {
                                Console.WriteLine("'b' is already chosen.");
                                break;
                            }
                            else 
                            { 
                                xoArray[0, 1] = xoLetter;
                                z++;
                                xoBool = true;
                                break;
                             }
                        case "c":
                            if ((xoArray[0, 2] == "X") || (xoArray[0, 2] == "O"))
                            {
                                Console.WriteLine("'c' is already chosen.");
                                break;
                            }
                            else
                            {
                                xoArray[0, 2] = xoLetter;
                                z++;
                                xoBool = true;
                                break;
                            }
                        case "d":
                            if ((xoArray[1, 0] == "X") || (xoArray[1, 0] == "O"))
                            {
                                Console.WriteLine("'d' is already chosen.");
                                break;
                            }
                            else
                            {
                                xoArray[1, 0] = xoLetter;
                                z++;
                                xoBool = true;
                                break;
                            }
                        case "e":
                            if ((xoArray[1, 1] == "X") || (xoArray[1, 1] == "O"))
                            {
                                Console.WriteLine("'e' is already chosen.");
                                break;
                            }
                            else
                            {
                                xoArray[1, 1] = xoLetter;
                                z++;
                                xoBool = true;
                                break;
                            }
                        case "f":
                            if ((xoArray[1, 2] == "X") || (xoArray[1, 2] == "O"))
                            {
                                Console.WriteLine("'f' is already chosen.");
                                break;
                            }
                            else
                            {
                                xoArray[1, 2] = xoLetter;
                                z++;
                                xoBool = true;
                                break;
                            }
                        case "g":
                            if ((xoArray[2, 0] == "X") || (xoArray[2, 0] == "O"))
                            {
                                Console.WriteLine("'g' is already chosen.");
                                break;
                            }
                            else
                            {
                                xoArray[2, 0] = xoLetter;
                                z++;
                                xoBool = true;
                                break;
                            }
                        case "h":
                            if ((xoArray[2, 1] == "X") || (xoArray[2, 1] == "O"))
                            {
                                Console.WriteLine("'h' is already chosen.");
                                break;
                            }
                            else
                            {
                                xoArray[2, 1] = xoLetter;
                                z++;
                                xoBool = true;
                                break;
                            }
                        case "i":
                            if ((xoArray[2, 2] == "X") || (xoArray[2, 2] == "O"))
                            {
                                Console.WriteLine("'i' is already chosen.");
                                break;
                            }
                            else
                            {
                                xoArray[2, 2] = xoLetter;
                                z++;
                                xoBool = true;
                                break;
                            }
                        default:
                            Console.WriteLine("must be a lowercase a through i");
                            break;
                    }
                } 

                //check logic going vertically because it doesnt work
                if (((xoArray[0, 0] == xoArray[0, 1]) && (xoArray[0, 1] == xoArray[0, 2])) ||
                    ((xoArray[1, 0] == xoArray[1, 1]) && (xoArray[1, 1] == xoArray[1, 2])) ||
                    ((xoArray[2, 0] == xoArray[2, 1]) && (xoArray[2, 1] == xoArray[2, 2])) ||
                    ((xoArray[0, 0] == xoArray[1, 0]) && (xoArray[1, 0] == xoArray[2, 0])) ||
                    ((xoArray[0, 1] == xoArray[1, 1]) && (xoArray[1, 1] == xoArray[2, 1])) ||
                    ((xoArray[0, 2] == xoArray[1, 2]) && (xoArray[1, 2] == xoArray[2, 2])) ||
                    ((xoArray[0, 0] == xoArray[1, 1]) && (xoArray[1, 1] == xoArray[2, 2])) ||
                    ((xoArray[2, 0] == xoArray[1, 1]) && (xoArray[1, 1] == xoArray[0, 2])))

                     {
                        Console.WriteLine(" [" + xoArray[0, 0] + "][" + xoArray[0, 1] + "][" + xoArray[0, 2] + "]");
                        Console.WriteLine(" [" + xoArray[1, 0] + "][" + xoArray[1, 1] + "][" + xoArray[1, 2] + "]");
                        Console.WriteLine(" [" + xoArray[2, 0] + "][" + xoArray[2, 1] + "][" + xoArray[2, 2] + "]");
                        Console.WriteLine("Congrats, player " + xoLetter + "! You have won the game!!");
                        break;
                    }

                if (z == 9)
                {
                    Console.WriteLine(" [" + xoArray[0, 0] + "][" + xoArray[0, 1] + "][" + xoArray[0, 2] + "]");
                    Console.WriteLine(" [" + xoArray[1, 0] + "][" + xoArray[1, 1] + "][" + xoArray[1, 2] + "]");
                    Console.WriteLine(" [" + xoArray[2, 0] + "][" + xoArray[2, 1] + "][" + xoArray[2, 2] + "]");
                    Console.WriteLine("Nobody wins. Thanks for playing!");
                    break;
                }

                if (xoLetter == "X")
                { 
                    xoLetter = "O";
                } 
                else 
                {
                    xoLetter = "X"; 
                }

            xoBool = false;
            Console.Clear();
            }

            Console.ReadKey();                    
        }
    }
}

