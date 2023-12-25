Introduction:
    I have been assigned to create a data warehouse for Bloomberg to analyze FX deals. The purpose of this 
file is to fully document the steps I have initiated and taken to solve the assignment as per the requirements 
been set. The project has been implemented in three main core classes (Main, Deal and Functions) as documented bellow:

** Deal Class:
    Has all requested fields/ variables for the user.

** Functions Class:
Multiple functions have been created and called to go through the user journey from entering the input into
validating the date and saving it into the database:
    1- isValidDeal: 
    Before accepting the input we receive from the user, we have to validate that no required
    field is empty and using this function helps us to verify that.
    2- isUniqueIdUnique: 
    The function takes the id as a parameter to check if the id is unique or not
    (only accepted Ids that are unique)
    3- createDealFromUserInput: 
    This function has multiple aspects to cover
     * Allows the input to be taken from the user  
     * checks if the id entered is unique or not. 
     * Check  if the user choses from the available currencies.
     * After all the validations has passed, the input will be saved into the database.
     4- saveDealToDatabase: 
     the code I have written is connected to a database that I have created using phpmyadmin -sql. 
     The solution I have implemented in this code saves the input from the user into the database. 
     The database contains a table called "deals" which has all the needed variables as "columns", 
     so after the data is inserted, it will be saved into the table using the function.
** Main Class:
    The main class does the following:
    1- Let the user decide how many deals they would like to make.
    2- Creates an array that equals the size the user chooses.
    3- After all validation has been passed, the function for insering the data into the database will be 
       called.
