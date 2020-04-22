# Encrypt
Encrypt
 class Program
    {
        static string encrypt(string alphabet,string input)
        {
            int index;
            char[] arr = input.ToCharArray();
            for(int i=0;i<input.Length;i++)
            {
                for(int k=0;k<alphabet.Length;k++)
                {
                    if(input [i]==alphabet[k])
                    {
                        if (k > 23)
                        {
                            index = k - 24;
                        }
                        else
                        {
                            index = k + 2;
                        }
                        arr[i] = alphabet[index];
                    }


                }
            }
            string text = "";
            foreach(char item in arr)
            {
                text += item;
            }

            return  text;
        }
        
      

        static void Main(string[] args)
        {


            string alphabet = "abcdefghijklmnopqrstuvwxyz";
            string input = Console.ReadLine();
            Console.WriteLine(encrypt(alphabet,input));
        }
    }
}
