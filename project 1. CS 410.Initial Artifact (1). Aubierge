/*
    * Description: Assignment 5.2, Project 1, CS 410.
    *
    * Author: Aubierge Bikoi
    *
    * Date: 06/12/2022
    */

#include<iostream>
using namespace std;
// Declare and initialize global arrays for usernames, passwords, and clients
string usernames [] = {"j.smith", "s.brown", "r.garcia"};
string passwords [] = {"banana", "kitty", "amor"};
string clients [] = {"Bob Jones", "Sarah Davis", "Amy Friendly", "Johnny Smith", 
"Carol Spears"};
/*
 * Allows the user to change a client's service selection
 *
 */
void ChangeCustomerChoice() {
// Initialize local variables
int client_number = 0;
int service_choice = 0;
int k = 0;
// Prompt for and read the number of the client to be changed
cout << "Enter the number of the client that you wish to change." << endl;
cin >> client_number;
// Prompt for new choice selection and read input from user
cout << "Please enter the client's new service choice (1 = Brokerage, 2 = 
Retirement)" << endl;
cin >> service_choice;
// Iterates through the clients array to find a matching client number (array
index)
for (k = 0; k < sizeof(clients) ; ++k) {
if (client_number == k) {
cout << "Selected option: " << k << endl;
}
}
}
/*
 * Prompts user for a username and password.
 * Checks for the existence of each and then compares them
 * to determine if they match
 *
 * @return boolean: True if username and password are valid and match. False 
otherwise.
 *
 */
bool CheckUserPermissionAccess() {
 
// Declare local variables
string password;
string username;
int i = 0;
int j = 0;
bool match = false;
// Prompt user for username and read their input
cout << "Enter your username: ";
cin >> username;
// Prompt user for password and read input
cout << "Enter your password: ";
cin >> password;
// Search the usernames array for a matching string.
for (i = 0; i < sizeof(usernames) + 1; ++i) {
//If found break from the loop
if (username == usernames[i]) {
break;
}
// If not found, set i to a value greater than the length of the array
else if (i == sizeof(usernames)) {
// i = username array length + 2
i = (sizeof(usernames) + 2);
}
}
// Search the passwords array for a matching string
for (j = 0; j < sizeof(passwords) + 1; ++j) {
// If found, break from loop
if (password == passwords[j]) {
break;
}
// If not found, set j to value > array length
else if (j == sizeof(passwords)) {
// j = passwords array length + 1
j = (sizeof(passwords) + 1);
}
}
// Compare i and j
if (i == j) {
// If equal, return True
 match = true;
}
 return match;
}
/*
 * Displays the list of clients
 *
 */
void DisplayInfo() {
int l = 0;
// Iterates through each item in the clients array, printing each one 
preceded by a number starting with 1
for (l = 0; l < sizeof(clients); ++l) {
cout << l << ". " << clients[l] << endl;
}
}
int main() {
// Declare local variables
bool authentication = false;
bool exit = false;
int menu_choice = 0;
// Print welcome message
cout << "Hello! Welcome to our Investment Company." << endl;
 cout << "Program written by Aubierge Bikoi" << endl;
// Call the ChechUserPermissionAccess function until authentication passed
while (!authentication) {
authentication = CheckUserPermissionAccess();
if (authentication) {
break;
}
else {
cout << "Invalid Password. Please try again.";
break;
}
}
// The selection menu will display after each switch statement until the user
selects 3
while (!exit) {
cout << "What would you like to do?" << endl;
cout << "DISPLAY the client list (enter 1)" << endl;
cout << "CHANGE a client's choice (enter 2)" << endl;
cout << "EXIT the program (enter 3)" << endl;
cin >> menu_choice;
cout << "You chose " << menu_choice << endl;
switch (menu_choice) {
case 1 :
DisplayInfo();
break;
case 2 :
ChangeCustomerChoice();
break;
case 3 :
exit = true;
break;
}
}
return 0;
}