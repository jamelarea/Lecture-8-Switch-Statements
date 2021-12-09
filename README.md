Lecture 8 Switch Statements Part 1

EXERCISE BREAK

SLIDE 10, Continue?

        #include <iostream>
        using namespace std;

        int main()
        {
            cout << "Would you like to continue? (Y/N): "; //ask for input
            char answer; //variable for user answer
            cin >> answer; //get user input

            switch (answer) { //evaluate expression
            case 'Y': //Yes
            case 'y': //Yes
                cout << "Continue" << endl; //message if user enters Y/y
                break;
            case 'N': //No
            case 'n': //No
                cout << "Quit" << endl; //message if user enters N/n
                break;
            default: //other inputs besides Y/y (Yes) and N/n (No)
                cout << "Invalid Response" << endl;
            }
            return 0;
        }

SLIDE 11, Days of the Month
        
    #include <iostream>
    using namespace std;

    int main()
    {
        //variable
        int month;

        cout << "Months" << endl; //character output
        cout << "1: January\n2: February\n3: March\n4: April\n5: May\n6: June\n7: July\n8: August\n9: September\n10: October\n11: November\n12: December\n\nSelect a month: "; //character output (choices)
        cin >> month; //character input

        switch (month) {
        case 1: //January
            cout << "\nThere are 31 days in January" << endl;
            break;
        case 2: //February
            cout << "\nThere are 28 days in February" << endl; 
            break;
        case 3: //March
           cout << "\nThere are 31 days in March" << endl;
           break;
        case 4: //April
           cout << "\nThere are 30 days in April" << endl;
           break;
        case 5: //May
           cout << "\nThere are 31 days in May" << endl;
           break;
        case 6: //June
           cout << "\nThere are 30 days in June" << endl;
           break;
        case 7: //July
           cout << "\nThere are 31 days in July" << endl;
           break;
        case 8: //August
           cout << "\nThere are 31 days in August" << endl;
           break;
        case 9: //September
           cout << "\nThere are 30 days in September" << endl;
           break;
        case 10: //October
           cout << "\nThere are 31 days in October" << endl;
           break;
        case 11: //November
           cout << "\nThere are 30 days in November" << endl;
           break;
        case 12: //December
           cout << "\nThere are 31 days in December" << endl;
           break;
        default: //other inputs besides 1-12
           cout << "\nIncorrect input. Please select a month by choosing a number depending on their specified months below.";
        }
        return 0;
    }

Lecture 8 Exercise

SLIDE 2, Days of the Month

    #include <iostream>
    using namespace std;

    int main()
    {
        //variable
        int month;

        cout << "Months" << endl; //character output
        cout << "1: January\n2: February\n3: March\n4: April\n5: May\n6: June\n7: July\n8: August\n9: September\n10: October\n11: November\n12: December\n\nSelect a month: "; //character output (choices)
        cin >> month; //character input

        switch (month) {
        case 1: //January
            cout << "\nThere are 31 days in January" << endl;
            break;
        case 2: //February
            cout << "\nThere are 28 days in February" << endl; 
            break;
        case 3: //March
           cout << "\nThere are 31 days in March" << endl;
           break;
        case 4: //April
           cout << "\nThere are 30 days in April" << endl;
           break;
        case 5: //May
           cout << "\nThere are 31 days in May" << endl;
           break;
        case 6: //June
           cout << "\nThere are 30 days in June" << endl;
           break;
        case 7: //July
           cout << "\nThere are 31 days in July" << endl;
           break;
        case 8: //August
           cout << "\nThere are 31 days in August" << endl;
           break;
        case 9: //September
           cout << "\nThere are 30 days in September" << endl;
           break;
        case 10: //October
           cout << "\nThere are 31 days in October" << endl;
           break;
        case 11: //November
           cout << "\nThere are 30 days in November" << endl;
           break;
        case 12: //December
           cout << "\nThere are 31 days in December" << endl;
           break;
        default: //other inputs besides 1-12
           cout << "\nIncorrect input. Please select a month by choosing a number depending on their specified months below.";
        }
        return 0;
    }

SLIDE 3, Fuel me Up
    
    #include <iostream>
    using namespace std;

    int main()
    {
        //variable
        char answer;

        cout << "Do you need fuel?\nY for Yes, N for No: "; //extraction operator
        cin >> answer; //insertion operator

        if (answer == 'Y')
        {
            //variables
            char fuel;
            int litres;

            cout << "\nSelect a type of fuel\nP for Petrol, D for Diesel: "; //character output
            cin >> fuel; //character input

            switch (fuel) {
            case 'P': //Petrol
            case 'p': //Petrol
                cout << "\nType of Fuel: Petrol" << endl; //character output

                cout << "Enter the amount of litres: "; //character output
                cin >> litres; //character input

                cout << "\nCharge = " << litres * 0.8 << " AED\n\nThank you for using our automatic fuel filling service." << endl; //formula for charge in Petrol
                break;
            case 'D':
            case 'd':
                cout << "\nType of Fuel: Diesel" << endl; //character output

                cout << "Enter the amount of litres: "; //character output
                cin >> litres; //character input

                cout << "\nCharge = " << litres * 0.5 << " AED\n\nThank you for using our automatic fuel filling service." << endl; //formula for charge in Diesel

                break;
            default: //other inputs besides P (Petrol) and D (Diesel)
                cout << "\nInvalid Input. " << endl;
            }
        }
        else //if not Y (Yes)
        {
            cout << "\nYou do not need fuel." << endl; //N for No
        }
        return 0;
    }
  
SLIDE 4, Switching Temperature
      
      #include <iostream>
      using namespace std;
  
      int main()
      {
          //variable
          int temp;

          cout << "Temperature Converter\n\nPlease choose\n1: Celcius to Fahrenheit 2: Fahrenheit to Celcius: "; //character output (choices)
          cin >> temp; //character input

          switch (temp)
          {
          case 1: //C to F
              cout << "\n1: Celsius to Fahrenheit" << endl; //label, shows the user that they picked conversion C to F

              cout << "Enter the temperature (C): "; //character output
              cin >> temp; //character input

              cout << "\nTemperature (F)= " << (temp = (temp * 9 / 5) + 32); //shows the converted temperature in Fahrenheit using the formula (C to F)
              break;
          case 2: //F to C
              cout << "\n2: Fahrenheit to Celsius" << endl; //label, shows the user that they picked conversion F to C

              cout << "Enter the temperature (F): "; //character output
              cin >> temp; //character input

              cout << "\nTemperature is (C)= " << (temp = (32 - 32) * 5 / 9); //shows the converted temperature in Celsius using the formula (F to C)
              break;
          default: //other inputs besides 1 (C to F) and 2 (F to C)
              cout << "\nInvalid Input";
              break;
          }
          return 0;
      }

SLIDE 5, Bonus: Switch Grade Calculator
      
      #include <iostream>
      #include <string>
      using namespace std;
  
      int main()
      {
          // variables
          string name;
          int grade;

          cout << "Enter the student's full name: "; //character output
          getline (cin, name); //character input, getline is used to read a string or a line from an input stream

          cout << "\nEnter the student's grade: "; //character output
          cin >> grade; //character input

          //checks if the score is valid or not
          if (grade < 0 || grade>100) //the grade to be inputted should be 0-100
          {
              cout << "Invalid input. Please enter the student's grade." << endl;
          }

          //show the student's grade depending on what the user's inputted
          switch (grade/10)
          {
          case 10: //100
          case 9: //90
          case 8: //80
              cout << "\nStudent's grade: A"; //greater than or equal to 80
              break;
          case 7: //70
              cout << "\nStudent's grade: B"; //between 70 and 79
              break;
          case 6: //60
              cout << "\nStudent's grade: C"; //between 60 and 69
              break;
          case 5: //50
              cout << "\nStudent's grade: D"; //between 50 and 59
              break;
          case 4: //40
              cout << "\nStudent's grade: E"; //between 40 and 49
              break;
          default: //less than 40
              cout << "\nStudent's grade: F"; //less than 40
          }
          return 0;
      }  
 
Lecture 8 Switch Statements Part 2
 
SLIDE 7, Code
 
        #include <iostream>
        using namespace std;

        int main()
        {
            //variable
            char input;

            cout << "What is the capital of France?\n\nA. Abu Dhabi\nB. Manila\nC. Paris\nD. Rome"; //character output (choices)
            cout << "\n\nAnswer: "; //character output
            cin >> input; //character input

            switch (input)
            {
            case 'A': //Abu Dhabi
            case 'a': //Abu Dhabi
            case 'B': //Manila
            case 'b': //Manila
            case 'D': //Rome
            case 'd': //Rome
                cout << "\nSorry, your answer is wrong.";
                break;
            case 'C': //Paris
            case 'c': //Paris
                cout << "\nCongratulations! your answer is correct.";
                break;
            default: //other inputs besides A, B, C, D
                cout << "\nPlease choose a letter from the given multiple choice.";
            return 0;
            }
        }

SLIDE 10, Code

        #include <iostream>
        using namespace std;

        int main()
        {
            //variable
            int side;

            cout << "Enter the number to see the shape name\n\nMinimum: 3 sides\nMaximum: 10 sides\n\nNumber of sides: "; //character output
            cin >> side; //character input

            //shows the name of the shape depending on what the user's inputted
            switch (side)
            {
            case 3: //3 sides
                cout << "\nA Triangle has " << side << " sides" << endl;
                break;
            case 4: //4 sides
                cout << "\nA quadrilateral has " << side << " sides" << endl;
                break;
            case 5: //5 sides
                cout << "\nA Pentagon has " << side << " sides" << endl;
                break;
            case 6: //6 sides
                cout << "\nA Hexagon has " << side << " sides" << endl;
                break;
            case 7: //7 sides
                cout << "\nA Heptagon has " << side << " sides" << endl;
                break;
            case 8: //8 sides
                cout << "\nAn Octagon has " << side << " sides" << endl;
                break;
            case 9: //9 sides
                cout << "\nA Nonagon has " << side << " sides" << endl;
                break;
            case 10: //10 sides
                cout << "\nA Decagon has " << side << " sides" << endl;
                break;
            default: //other inputs besides 1-10
                cout << "\nInvalid input. Please enter a correct value.";
            }
            return 0;
        }
        
EXERCISE BREAK

SLIDE 18, Write the code for Switching Temperature

        #include <iostream>
        using namespace std; 

        int main()
        {
            //variable
            int temp;

            cout << "Temperature Converter\n\nPlease choose\n1: Celcius to Fahrenheit 2: Fahrenheit to Celcius: "; //character output (choices)
            cin >> temp; //character input

            switch (temp)
            {
            case 1: //C to F
                cout << "\n1: Celsius to Fahrenheit" << endl; //label, shows the user that they picked conversion C to F

                cout << "Enter the temperature (C): "; //character output
                cin >> temp; //character input

                cout << "\nTemperature (F)= " << (temp = (temp * 9 / 5) + 32); //shows the converted temperature in Fahrenheit using the formula (C to F)
                break;
            case 2: //F to C
                cout << "\n2: Fahrenheit to Celsius" << endl; //label, shows the user that they picked conversion F to C

                cout << "Enter the temperature (F): "; //character output
                cin >> temp; //character input

                cout << "\nTemperature is (C)= " << (temp = (32 - 32) * 5 / 9); //shows the converted temperature in Celsius using the formula (F to C)
                break;
            default: //other inputs besides 1 (C to F) and 2 (F to C)
                cout << "\nInvalid Input";
                break;
            }
            return 0;
        }
