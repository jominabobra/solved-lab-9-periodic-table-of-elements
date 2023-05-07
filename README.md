Download Link: https://assignmentchef.com/product/solved-lab-9-periodic-table-of-elements
<br>
<p class="ui header product-top-header" title="Lab 9 Periodic table of elements Solution">Lab 9Periodic table of elementsNOTE: Do not forget to fill out the class survey: Click HereObjectivesLearn how to read from and write to filesPractice using data structuresPractice top-down program designPractice re-using codeOverviewFor this lab, you will implement a program that can output information about any element in the periodic table of elements.

Requirements:

Read in a comma-separated values text file that contains the information about the elements in the periodic table.Save those elements in a data structure for further processing.Accept command-line parameters:Program arguments shall be the chemical symbols for wish the user wants more informationOptionally, the user may provide as the first program argument, the name of a file to write the information out to.Print out, or write to a file, information about the elements requested.Data structure for elementsYou will need to declare a data structure to hold the information about the chemical elements. Your structure will have the following components:

Atomic Number (integer)Chemical Symbol (string)Name (string)Atomic Weight (floating point number)State at room temp (string)Bonding type (string)Year discovered (string)Read in fileFirst, download the element database file by clicking here: element_db.csv.

Save this file in the same directory as the source code for your lab.The first thing your program should do is read in the element_db.csv file, line by line. Every line of the file represents one element in the periodic table of elements.Open the .csv file for reading a text file, and read in every line of the file using the function fgets.The file in csv format, which means the data fields are separated by commas. Use the function strtok to extract the data field by field.You can use the function atoi to convert a string to an integer.The function atof can be used to convert a string to a floating point number.Save all of the elements scanned in into an array for further processing.Remember to close the file once you have read in the contents.Process program argumentsYour program needs to accept one or more command line program arguments. If the program is called with no arguments, it should print this error message and then exit:

ERROR: Please provide at least one program argument.

Each of the arguments provided to the program should be the chemical symbol of a chemical to look up information about (with one exception, mentioned below).

The program should check the first argument provided to see if it contains a . character. If it does, that argument may be assumed to be a filename, and the program should write the output to that file. You may want to use the function strchr to search for the . character.

For every chemical symbol argument, the program should look up the relevant information about that element.

You can do this by looping through the array of elements, using strcmp to check if the chemical symbol matches the program argument.

When you find a matching element, either print the information to the screen or write it out to the output file, depending if that first argument was a filename or not.Note that you should be able to use the same function to accomplish this regardless of the target output stream, by using fprintf with the output file pointer or the built-in file pointer stdout.If no element was found for the input symbol, print a message like this:

WARNING: No such element: [symbol]

(replace [symbol] with the name of the symbol that could not be found).

Print out the element in a similar format to the one used for Lab 7:

—————| 3 6.9410| Li Lithium| solid| metallic| Found: 1817—————

Print the atomic number and atomic weight on the top line, separated by a ‘t’ character.Print the chemical symbol and name on the next line, separated by a ‘t’ character.Print the physical state on the next linePrint the bonding type on the line after thatPrint the date discovered on the last line, after the word “Found: “.Print the top and bottom with the dash – character, and side of the box using the pipe | character.Remember to close the output file once you have finished processing all of the command-line arguments.

Example ExecutionNo program arguments

[esus] $ ./lab9ERROR: Please provide at least one program argument.

Output to screen: Iron, Silver, Carbon, Potassium

[esus] $ ./lab9 Fe C Ag K—————| 26 55.8450| Fe Iron| solid| metallic| Found: Ancient——————————| 6 12.0107| C Carbon| solid| covalent network| Found: Ancient——————————| 47 107.8682| Ag Silver| solid| metallic| Found: Ancient——————————| 19 39.0983| K Potassium| solid| metallic| Found: 1807—————

Output to screen: Mercury, Phosphorus, Flourine

[esus] $ ./lab9 Hg P F—————| 80 200.5900| Hg Mercury| liquid| metallic| Found: Ancient——————————| 15 30.9738| P Phosphorus| solid| covalent network| Found: 1669——————————| 9 18.9984| F Fluorine| gas| atomic| Found: 1670—————

Output to file: Lithium, Aluminum, Iodine saved to file output.txt (note: no output is printed to screen).

[esus] $ ./lab9 output.txt Li Al I[esus] $

Content of output.txt:

[esus] $ cat output.txt—————| 3 6.9410| Li Lithium| solid| metallic| Found: 1817——————————| 13 26.9815| Al Aluminum| solid| metallic| Found: Ancient——————————| 53 126.9045| I Iodine| solid| covalent network| Found: 1811—————

Program arguments have invalid symbol name:

[esus] $ ./lab9 S Hh H—————| 16 32.0650| S Sulfur| solid| covalent network| Found: Ancient—————WARNING: No such element: Hh—————| 1 1.0079| H Hydrogen| gas| diatomic| Found: 1766—————

Compile &amp; TestCompile your program using this gcc command. c99 is a shortcut for running gcc -std=c99, which uses the C99 standard instead of the default C89 standard.

$ c99 -Wall lab9.c -o program9

NOTE: Make sure you output what is expected, nothing more and nothing less.You should use the Lab Grader tool to check your work. This assignment name is ‘lab9’, so you should run the tool like this (substitute your own filename):

./grade lab9 last_first_lab9.c

NOTE: The grading materials for this lab are not currently available. They will be posted shortly.ResourcesYou should attend the Friday Lab session to seek assistance from the TAs and CAs.For specific questions, attend the weekly lab session or attend the TA’s office hours.You are encouraged to use resources or tutorials on the internet to learn unix or C. Check the class resource list for some links to resources.SubmissionAssigned: April 18thLab Day: April 20thDue Date: April 25th, 8:00am

Make sure you included ample and informative comments – it is 20% of your grade!Rename your C file to last_first_lab9.c and substitute your last and first name.

NOTE: If you fail to follow the above file naming conventions, your program cannot be graded automatically and you will lose points.Submit your .c file to the D2L Dropbox for Lab 9. Detailed Instructions

NOTE: Submit only your C file to D2L. Do not submit your object file or executable program. Do not archive (e.g. zip) your file.Each student will complete and submit this assignment individually. Submit your work on or before the deadline as late work will receive a 50% penalty. Labs submitted more than 24 hours late will not be accepted.