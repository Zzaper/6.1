  public static void main(String[] args) {

        Scanner scr = new Scanner(System.in);

        int numbr = Integer.parseInt(scr.nextLine());
        int firstNumber = numbr / 100;
        int secondNumber = (numbr / 10) % 10;
        int thitdNumber = numbr % 10;
        int n = firstNumber + secondNumber;
        int m = firstNumber + thitdNumber;
        for (int i = 1; i <= n; i++)
        {
            for (int j = 1; j <= m; j++)
            {

                if (numbr % 5 == 0) {
                    numbr = numbr - firstNumber;
                } else if (numbr % 3 == 0) {
                    numbr = numbr - secondNumber;
                } else if ((numbr % 5 != 0) && (numbr % 3 != 0)) {
                    numbr = numbr + thitdNumber;
                }
                System.out.printf(numbr + " ");
                if (j < m)
                {
                    System.out.print(" ");
                }
            }

        }
