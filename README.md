Introduction:
    I have been assigned to create a data warehouse for Bloomberg to analyze FX deals. The purpose of this file is to fully document the steps I have initiated and taken to solve the assignment as per the requirements been set. The project has been implemented in three main core classes (Main, Deal, and Functions) as documented below:

** Deal Class:
    Represents the structure of a single FX deal, holding the necessary fields.

** Functions Class:
    The `Functions` class contains multiple functions to facilitate the user journey from entering input to validating the data and saving it into the database:
  
    1. `isValidDeal`:
       - Before accepting user input, this function ensures that no required field is empty.
    2. `isUniqueIdUnique`:
       - Takes an ID as a parameter and checks its uniqueness, only accepting unique IDs.

    3. `createDealFromUserInput`:
       - Allows the user to input data.
       - Checks the uniqueness of the entered ID.
       - Ensures the user selects from available currencies.
       - After passing all validations, the input is saved into the database.

    4. `saveDealToDatabase`:
       - Connects to a database created using phpMyAdmin SQL.
       - Saves user input into the "deals" table in the database.

** Main Class:
    The `Main` class serves as the entry point for the program and performs the following steps:
    1. Lets the user decide how many deals they would like to make.
    2. Creates an array with a size equal to the user's choice.
    3. After all validations have been passed, the function for inserting the data into the database is called.
