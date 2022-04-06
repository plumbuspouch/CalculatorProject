# CalculatorProject
Calculator Project for Fundamentals of programming

public class MyProgram extends ConsoleProgram
{
    //constructors
    int operationSelection;
    int service;
    String base;
    
    
    public void run()
    {
        Calculator calculator = new Calculator();
        System.out.println("Hi, I'm calulator. I'm excited to help you today!");
        while(operationSelection != 8)
        {
            if(operationSelection == 8)
            {
                break;
            }
            
            //Here is the list of Ops the user can choose from.

            System.out.println("Here is the list of operations I can perform for you: ");
            System.out.println("");
            System.out.println("\t1 - Add");
            System.out.println("\t2 - Subtract");
            System.out.println("\t3 - Multiply");
            System.out.println("\t4 - Divide");
            System.out.println("\t5 - Factorial");
            System.out.println("\t6 - Find the Area of a Triangle");
            System.out.println("\t7 - Covert Decimal to a Different Number System");
            System.out.println("\t8 - Exit");
            System.out.println("");
            
            //Where they choose the Op they want me to perform. 
            operationSelection = readInt ("Please choose one of the options from the Operations Menu above: ");
            
            //helping to create space and easier to read formating
            System.out.println("");
            System.out.println("");
            
            /*this section will only populate if 1-4 is chosen in the main
            operations menu. The section below is for Addition, Subtraction
            multiply, & divide. */
            if (operationSelection == 1 || operationSelection == 2 || operationSelection == 3 || operationSelection == 4)
            {
                //Here is the list of formats the user can choose from.
                System.out.println("Here are the number formats you can use: ");
                System.out.println("\t1 - Integer");
                System.out.println("\t2 - Double");
        
            
                System.out.println("");
            
                //Where they choose the format they want to use.
                int formatSelection = readInt ("Please choose one of the options from the Format Menu above: ");
            
                System.out.println("");
            
            
            //For Addition of Interger
            if(operationSelection == 1 && formatSelection == 1)
            {
                int userIntNumber1 = readInt("Please enter your first Integer for your equation:");
                int userIntNumber2 = readInt("Please enter your second Integer for your equation:");
                int addIResult = calculator.addI(userIntNumber1, userIntNumber2);
                
                System.out.println("The addition operation on " + userIntNumber1 + " + " + userIntNumber2 + " = " + addIResult);
                System.out.println("");
            }
            
            //For Addition of Double
            else if(operationSelection == 1 && formatSelection == 2)
            {
                double userDoubleNumber1 = readDouble("Please enter your first Double for your equation:");
                double userDoubleNumber2 = readDouble("Please enter your second Double for your equation:");
                double addDResult = calculator.addD(userDoubleNumber1, userDoubleNumber2);
                
                System.out.println("The addition operation on " + userDoubleNumber1 + " + " + userDoubleNumber2 + " = " + addDResult);
                System.out.println("");
            }
            
            //For Subtraction of Interger
            else if(operationSelection == 2 && formatSelection == 1)
            {
                int userIntNumber1 = readInt("Please enter your first Integer for your equation:");
                int userIntNumber2 = readInt("Please enter your second Integer for your equation:");
                int subIResult = calculator.subtractI(userIntNumber1, userIntNumber2);
                
                System.out.println("The addition operation on " + userIntNumber1 + " - " + userIntNumber2 + " = " + subIResult);
                System.out.println("");
            }
            
            //For Subtraction of Double
            else if(operationSelection == 2 && formatSelection == 2)
            {
                double userDoubleNumber1 = readDouble("Please enter your first Double for your equation:");
                double userDoubleNumber2 = readDouble("Please enter your second Double for your equation:");
                double subDResult = calculator.subtractD(userDoubleNumber1, userDoubleNumber2);
                
                System.out.println("The addition operation on " + userDoubleNumber1 + " - " + userDoubleNumber2 + " = " + subDResult);
                System.out.println("");
            }
            
            //For Multiplication of Interger
            else if(operationSelection == 3 && formatSelection == 1)
            {
                int userIntNumber1 = readInt("Please enter your first Integer for your equation:");
                int userIntNumber2 = readInt("Please enter your second Integer for your equation:");
                int mutliplyIResult = calculator.multiplyI(userIntNumber1, userIntNumber2);
                
                System.out.println("The addition operation on " + userIntNumber1 + " x " + userIntNumber2 + " = " + mutliplyIResult);
                System.out.println("");
            }
            
            //For Multiplication of Double
            else if(operationSelection == 3 && formatSelection == 2)
            {
                double userDoubleNumber1 = readDouble("Please enter your first Double for your equation:");
                double userDoubleNumber2 = readDouble("Please enter your second Double for your equation:");
                double mutliplyDResult = calculator.multiplyD(userDoubleNumber1, userDoubleNumber2);
                
                System.out.println("The addition operation on " + userDoubleNumber1 + " x " + userDoubleNumber2 + " = " + mutliplyDResult);
                System.out.println("");
            }
            
            //For Division of Interger
            else if(operationSelection == 4 && formatSelection == 1)
            {
                int userIntNumber1 = readInt("Please enter your first Integer for your equation:");
                int userIntNumber2 = readInt("Please enter your second Integer for your equation:");
                int divideIResult = calculator.divideI(userIntNumber1, userIntNumber2);
                
                System.out.println("The addition operation on " + userIntNumber1 + " / " + userIntNumber2 + " = " + divideIResult);
                System.out.println("");
            }
            
            //For Division of Double
            else if(operationSelection == 4 && formatSelection == 2)
            {
                double userDoubleNumber1 = readDouble("Please enter your first Double for your equation:");
                double userDoubleNumber2 = readDouble("Please enter your second Double for your equation:");
                double divideDResult = calculator.divideD(userDoubleNumber1, userDoubleNumber2);
                
                System.out.println("The addition operation on " + userDoubleNumber1 + " / " + userDoubleNumber2 + " = " + divideDResult);
                System.out.println("");
            }
            
            System.out.println("");
            }
            
            //Factorial Code
            if (operationSelection == 5)
            {
                int userIntNumber1 = readInt("What number would you like to find the factorial of? ");
                int factorialResult = calculator.factorial(userIntNumber1);
                
                System.out.println("The Factorial of " + userIntNumber1 + " is: " +  factorialResult);
                System.out.println("");
            }
            
            //Finding the Area of a triangle Code
            if (operationSelection == 6)
            {
                double triangleBase = readDouble("What is the length of the triangle base? ");
                double triangleHeight = readDouble("What is the height of the triangle? ");
                double triangleDegree = readDouble("What are the degrees of the triangle? ");
                double areaResult = calculator.areaOfTriangle(triangleBase, triangleHeight, triangleDegree);
                
                System.out.println("The Area of the Triangle is: " +  areaResult + " sq. units. ");
                System.out.println("");
            }
            
            //Coverting Decimal
            if (operationSelection == 7)
            {
                int decimalNum = readInt("What is the decimal number you'd like to convert? ");
                int numSystem = readInt("What base of the number system would you like to convert it to? ");
                String convertDecimal = calculator.convert(decimalNum, numSystem);
                 
                System.out.println(decimalNum + " converted to a base of "+ numSystem + " is " +  convertDecimal);
                System.out.println("");
            }
            
        }
    //End Message
    System.out.println("Thank you for using my functions.");
    
    //this code is just for fun to get a feel of how the user liked the calculator
        System.out.println("");
        while(service < 5)
        {
            System.out.println("");
            service = readInt("On a scale of 1 to 5 (1 being poor and 5 being fabulous) how satisified are you with my operations? ");
            if(service < 1)
            {
                System.out.println("");
                System.out.println("Now you're just being mean.. try again.");
            }
            else if(service == 1)
            {
                System.out.println("");
                System.out.println("Oh no. I'm sorry I didn't meet your needs. Please take it up with my creator and try again. ");
            }
            else if(service == 2)
            {
                System.out.println("");
                System.out.println("Hmmm...maybe you want to try again? ");
            }
            else if(service == 3)
            {
                System.out.println("");
                System.out.println("So you're saying I'm not the worst, but you're also saying I'm not the best. I think you better try again.");
            }
            else if(service == 4)
            {
                System.out.println("");
                System.out.println("You meant five didn't you? Perhaps you'd like to try again? ");
            }
            else if(service == 5)
            {
                System.out.println("");
                System.out.println("Yea, I'm pretty good like that. Thanks for recognizing");
            }
            else if(service > 6)
            {
                System.out.println("");
                System.out.println("Now you're just flattering me.... Stop. (Just kidding, don't stop.) ");
            }
            if(service > 5)
            {
                break;
            }
        }
    }
    
    
    //Calcuator Class Code:
    
  public class Calculator
{
    // constructors
    String convertDecimal;
    
    //int return types for equations. 
    public int addI (int userIntNumber1, int userIntNumber2)
    {
        int addIResult = userIntNumber1 + userIntNumber2;
        
        return addIResult;
    }
    
    public int subtractI (int userIntNumber1, int userIntNumber2)
    {
        int subIResult = userIntNumber1 - userIntNumber2;
        
        return subIResult;
    }
    
    public int multiplyI (int userIntNumber1, int userIntNumber2)
    {
        int multiplyIResult = userIntNumber1 * userIntNumber2;
        
        return multiplyIResult;
    }
    
    public int divideI (int userIntNumber1, int userIntNumber2)
    {
        int divideIResult = userIntNumber1 / userIntNumber2;
        
        return divideIResult;
    }
    
    
    //double return types for equations.
    public double addD (double userDoubleNumber1, double userDoubleNumber2)
    {
        double addDResult = userDoubleNumber1 + userDoubleNumber2;
        
        return addDResult;
    }
    
    
    public double subtractD (double userDoubleNumber1, double userDoubleNumber2)
    {
        double subDResult = userDoubleNumber1 - userDoubleNumber2;
        
        return subDResult;
    }
    
    public double multiplyD (double userDoubleNumber1, double userDoubleNumber2)
    {
        double mutliplyDResult = userDoubleNumber1 * userDoubleNumber2;
        
        return mutliplyDResult;
    }
    
    public double divideD (double userDoubleNumber1, double userDoubleNumber2)
    {
        double divideDResult = userDoubleNumber1 / userDoubleNumber2;
        
        return divideDResult;
    }
    
    //factorial operation and return
    public int factorial (int userIntNumber1)
    {
        int factorialResult = 1;
        for(int i = 1;i <= userIntNumber1;i++)
        {
            factorialResult *=i;
        }
        
        return factorialResult;
    }
    
    //finding the area of a triangle operation
    public double areaOfTriangle (double triangleBase, double triangleHeight, double triangleDegree )
    {
        //the step below step initializes Pi
        double pi = 3.141592653589793;
        double triangleRadiants = multiplyD(triangleDegree, pi) /180;
        double triangleDegrees = Math.sin(triangleRadiants);
        double sideResult = multiplyD(triangleBase, triangleHeight);
        double finalSideResult = multiplyD(.5, sideResult);
        double areaResult = multiplyD(triangleDegrees, finalSideResult);
        
        return areaResult;
    }
    
    
    //Converting decimal to another number system. 
    public String convert (int decimalNum, int numSystem)
    {
        //https://www.programiz.com/java-programming/examples/binary-decimal-convert 
        //this site helped me perform my code
        if(numSystem == 2)
        {   
            System.out.println("Converting Decimal to Binary: ");
            //intitializing
            String binaryNum ="";
            int remainder = 0, i = 1, step = 1;
            while(decimalNum != 0)
            {
                remainder = decimalNum % 2;
                System.out.println("Step " + step++ + ": " + decimalNum + "/2 ");
                System.out.println("Quotient = " + decimalNum/2 + ", remainder = " + remainder);
                decimalNum /=2;
                
                binaryNum = remainder + binaryNum;
                i *= 10;
                
            }
            
            return binaryNum;
        }
        
        else if(numSystem == 8)
        {   
            System.out.println("Converting Decimal to Octal: ");
            //intitializing
            String octalNum = "";
            int remainder = 0, i = 1, step = 1;
            while(decimalNum != 0)
            {
                remainder = decimalNum % 8;
                System.out.println("Step " + step++ + ": " + decimalNum + "/8 ");
                System.out.println("Quotient = " + decimalNum/8 + ", remainder = " + remainder);
                decimalNum /=8;
                
                octalNum = remainder + octalNum;
                i *= 10;
                
            }
            
            return octalNum;
        }
        
        else if(numSystem == 16)
        {   
            System.out.println("Converting Decimal to Hexidecimal: ");
            //intitializing
            String hexNum ="";
            int remainder = 0, i = 1, step = 1;
            String convRemainder = "";
            while(decimalNum != 0)
            {
                //Converting dec numbers to letters for hex
                remainder = decimalNum % 16;
                if(remainder == 1)
                {
                    convRemainder = "1";
                }
                else if(remainder == 2)
                {
                    convRemainder = "2";
                }
                else if(remainder == 3)
                {
                    convRemainder = "3";
                }
                else if(remainder == 4)
                {
                    convRemainder = "4";
                }
                else if(remainder == 5)
                {
                    convRemainder = "5";
                }
                else if(remainder == 6)
                {
                    convRemainder = "6";
                }
                else if(remainder == 7)
                {
                    convRemainder = "7";
                }
                else if(remainder == 8)
                {
                    convRemainder = "8";
                }
                else if(remainder == 9)
                {
                    convRemainder = "9";
                }
                else if(remainder == 10)
                {
                    convRemainder = "A";
                }
                else if(remainder == 11)
                {
                    convRemainder = "B";
                }
                else if(remainder == 12)
                {
                    convRemainder = "C";
                }
                else if(remainder == 13)
                {
                    convRemainder = "D";
                }
                else if(remainder == 14)
                {
                    convRemainder = "E";
                }
                else if(remainder == 15)
                {
                    convRemainder = "G";
                }
                else if(remainder == 16)
                {
                    convRemainder = "F";
                }
                System.out.println("Step " + step++ + ": " + decimalNum + "/16 ");
                System.out.println("Quotient = " + decimalNum/16 + ", remainder = " + convRemainder);
                decimalNum /=16;
                
                hexNum = convRemainder + hexNum;
                
                
                i *= 10;
                
                
                
            }
            
            return hexNum;
            
            
        }
        
        return convertDecimal;
    }
}  
    
