# rengeteg_for
 var numbers = new int[10];
            var paros = new int[10];
            Random rnd = new Random();
            int osszeg = 0;
            int negy = 0;
            bool heeet = false;
            bool ha_rom = false;
            for (int i = 0; i < numbers.Length; i++)
            {
                
                numbers[i] = rnd.Next(1, 10);
                
            }
            for (int i = 0; i < numbers.Length; i++)
            {
                Console.WriteLine(numbers[i]);
                
            }
            for (int i = 0; i < numbers.Length; i++)
            {
                osszeg += numbers[i];
            }
            for (int i = 0; i < numbers.Length; i++)
            {
                if (numbers[i] > 4)
                {
                    negy++;
                }
            }
            for (int i = 0; i < numbers.Length; i++)
            {
                if (numbers[i] % 7 == 0)
                {
                    heeet=true;
                    break;
                }
            }

            if (heeet == true)
            {
                Console.WriteLine("van benne 7-tel osztható");
            }
            else
            {
                Console.WriteLine("nincs benne 7-tel osztható");
            }


            for (int i = 0; i < paros.Length; i++)
            {
                if(numbers[i] % 2 == 0)
                {
                    paros[i] = numbers[i];

                }
            }
            Console.WriteLine("páros számok:");
            for (int i = 0; i < paros.Length; i++)
            {
                if(paros[i] != 0)
                {
                    Console.WriteLine(paros[i]);
                } 
            }
            for (int i = 0; i < numbers.Length; i++)
            {
                if(numbers[i] % 3 == 0)
                {
                    Console.WriteLine("az első 3-mal osztató: {0}", numbers[i]);
                    ha_rom = true;
                    break;
                }
                
            }
            if (ha_rom == false)
            {
                Console.WriteLine("nincs benne 3-mal osztaható");
            }
            
            Console.WriteLine("{0} darab szám van ami nagyobb mint 4", negy);
            Console.WriteLine("A számok összege: {0}", osszeg);
            Console.WriteLine("üsd meg a billentyűzetet (csak finoman!!!!!)");
            Console.ReadKey();
