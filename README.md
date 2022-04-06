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
    
