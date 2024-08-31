Random dice = new Random();
        Console.WriteLine("how many kinds of dice are there?");
        int dicen = Convert.ToInt16(Console.ReadLine());
        int ogdicen = dicen;

        int listspot = 0;
        double totalforaverage = 0;
        double average = 0;
        double total = 0;

        List<double> averages = new List<double>();
        List<int> sides = new List<int>();
        List<int> numdice = new List<int>();
        List<double> totals = new List<double>();

        string n = "n";
        string a = "a";
        string d = "d";

            while(dicen >= 1)
            {
                Console.WriteLine("are you rolling with advantage? (a for advantage, d for disadvantage and n for none(lowercase)");
            Console.WriteLine();
            string advantage = Convert.ToString(Console.ReadLine());
                if (advantage == a) { 
                
                    Console.WriteLine("how many sides should the dice have?");
                    int side1n = Convert.ToInt16(Console.ReadLine());
                    sides.Add(side1n);

                    Console.WriteLine("how many times should it roll?");
                    int roll1n = Convert.ToInt16(Console.ReadLine());
                    numdice.Add(roll1n);

                    Console.WriteLine("does this set have a modifier?");
                    double modifier = Convert.ToInt32(Console.ReadLine());
                    while (roll1n >= 1)
                    {
                        roll1n--;
                        int roll2 = dice.Next(1, side1n + 1);
                        int roll1 = dice.Next(1, side1n + 1);
                        double roll = Math.Max(roll1+modifier, roll2+modifier);
                        Console.Write("after doing the advantage thing you got ");
                        Console.WriteLine(roll);
                        total = total + Math.Max(roll1,roll2);
                        totalforaverage = totalforaverage + roll;
                    }
                        totals.Add(totalforaverage);
                        average = totalforaverage / numdice[listspot];
                        averages.Add(average);
                       
                        dicen--;
                        average = 0;
                        totalforaverage = 0;
                        listspot ++;
                    }
                
                else if (advantage == d)
                {
                    Console.WriteLine("how many sides should the dice have?");
                    int side1n = Convert.ToInt16(Console.ReadLine());
                    sides.Add(side1n);

                    Console.WriteLine("how many times should it roll?");
                    int roll1n = Convert.ToInt16(Console.ReadLine());
                    numdice.Add(roll1n);

                    Console.WriteLine("does this set have a modifier?");
                    double modifier = Convert.ToInt16(Console.ReadLine());

                    while (roll1n >= 1)
                    {
                        roll1n--;
                        int roll2 = dice.Next(1, side1n + 1);
                        int roll1 = dice.Next(1, side1n + 1);
                        double roll = Math.Min(roll1+modifier, roll2+modifier);
                        Console.Write("after doing the disadvantage thing you got " );
                        Console.WriteLine(roll);
                        total = total + Math.Min(roll1,roll2);
                        totalforaverage = totalforaverage + roll;
                        
                    }
                        totals.Add(totalforaverage);
                        average = totalforaverage / numdice[listspot];
                        averages.Add(average);
                        
                        dicen--;
                        average = 0;
                        totalforaverage = 0;
                        listspot ++;
                    }
                
           else if (advantage == n)
                {
                    Console.WriteLine("how many sides should the dice have?");

                    int side1n = Convert.ToInt16(Console.ReadLine());
                    sides.Add(side1n);

                    Console.WriteLine("how many times should it roll?");
                    int roll1n = Convert.ToInt16(Console.ReadLine());
                    numdice.Add(roll1n);

                    Console.WriteLine("does this set have a modifier?");
                    double modifier = Convert.ToInt16(Console.ReadLine());


                    while (roll1n >= 1)
                    { 
                        roll1n--;
                        double roll1 = dice.Next(1, side1n + 1) + modifier;
                        Console.WriteLine(roll1);
                        total = total + roll1;
                        totalforaverage = totalforaverage + roll1;
                    }
                    totals.Add(totalforaverage);
                    average = totalforaverage / numdice[listspot];
                    averages.Add(average);
                    
                    dicen--;
                    average = 0;
                    totalforaverage = 0;
                    listspot ++;
                }
                
               }
               listspot = 0;
            while(listspot<ogdicen){

                 Console.WriteLine("you rolled a total of " + totals[listspot] + " out of your " + numdice[listspot] + "d" + sides[listspot] + " and an average of " + averages[listspot]);
                        listspot++;
            }
