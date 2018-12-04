# HW2
// Name:Linda Hernandez
// Date:10/2/2018
// Class:COP2000/ T 6:30
// Assignment:Homework Assignment 2-A, Harvey's Room Calculator
// This program calculates the area of the room depending of the shape.

#include <iostream>
#include <iomanip>
using namespace std;

int main()
{
    int user_menu_input = 1-4;
  
   double room_length = 1;
   double room_width = 1;
   double room_radius = 1;
   const double PI = 3.14159
   
   // Constants for menu options
    const int SquareRoom = 1,
    const int RectangularRooom = 2,
    const int RoundRoom = 3,
    const int QuitOption = 4;
	
  // Display menu of room options
   cout << "Haverly's Room Calculator" << endl;
   cout << " ======Menu======" << endl;
   cout << " 1: Square Room " << endl;
   cout << " 2: Rectangle Room " << endl;
   cout << " 3: Round Room " << endl;
   cout << " 4: Quit " << endl;
   cout << "Please enter a Menu item: 1-4" << endl;
   cin >> user_menu_input;
  
  
   switch(user_menu_input)
   {
       case 1:
         // Square Room
         cout << "What is the length of the room in square feet?" << endl;
         cin >> room_length;
         while(room_lenth <= 0)
         {
             cout << "You inputed a wrong number. Please try again with a positive number."
             cin >> room_length;
         }
         cout << "The area  of the square room is " << (room_length * room_length) << " in square feet. " << endl;
         break;
        case 2:
         // Rectangle Room
         cout << "What is the length of the room in square feet?" << endl;
         cin >> room_length;
         while(room_length <= 0)
         {
             cout << "You inputed a wrong number. Please try again with a postive number."
             cin >> room_legnth;
         }
         cout << "What is the width of the room in square feet?" << endl;
         cin >> room_width;
         while(room_width <= 0)
         {
             cout << "You inputed a wrong number. Please try again with a postive number."
             cin >> room_width;
         }
         cout << "The area of the rectangle room is" << (room_legth * room_width) << "in square feet." << endl;
         break;
        
        case 3:
         // Round Room
         cout << "What is the raduis?" << endl;
         cin >> room_radius;
         while(room_radius <= 0)
         {
             cout << "You inputed a wrong number. Please try again with a postive number."
             cin >> room_radius;
         }
         cout << "The area of the round room is" << (PI * (room_radius^2)) << "in square feet." << endl;
         break;
        
        case 4:
         // Quit
         cout << "Thank you for using Haverly's Room Calculator." << endl;
         cout << "Now exiting Program." << endl;
         while(QuitOption <= 0)
         {
             cout << "Invalid input. Please try again."
             cin  >> QuitOption;
         }
         break;
         
        default: cout << "This is an invalid input...program exiting..." << endl;
   }
   return 0;
}
