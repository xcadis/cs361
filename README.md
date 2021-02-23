# cs361
**Population Generator Project - OSU Software Engineering CS361**

Purpose: This microservice will provide the population size given an input year and U.S. State. The input year will be limited to U.S. Census Data available through the ACS Datastore for years 2005-2019. 

**How to use:** 

  Program can run in three ways:
  
  1. Command Mode - In this mode, a user needs to submit an argument (the input file, input.csv, see below for formatting) when running the program from the command line. When executed the program will return an output file, output.csv, in the same respective folder where the program was run from. 

To launch in command mode, run: python3 population-generator.py input.csv

  2. Command Mode Feeding Into the Person Generator - In this mode, the population generator is used to communicate with the person generator, by running the person generator directly. In this case, the input.csv file is implied (i.e. needs to be created before executed) and needs to be in format that the Person Generator expects (not the format of the population generator). Once this option is executed, it will generate an output.csv file specific to the Person Generator. 
 
To launch in command mode, run: python3 population-generator.py request_person_generator 

  3. GUI Mode - In this mode, user needs to run the program without any arguments and a Tkinter GUI will launch accordingly. This GUI will allow users to submit state/year in order to generate the respective population size. User can run unlimited number of searches, all of which will be saved into output.csv file while also being printed to the GUI. 

To launch in GUI mode, run: python3 population-generator.py      (no arguments) 


**Sample Input File for Population Generator:**

input_year,input_state

2019,Alabama

2012,Colorado

2008,Colorado

**Sample Output File (to be generated in either Command or GUI launches) for Population Generator:**


input_year,input_state,output_population_size

2019,Alabama,4903185

2012,Colorado,5187582

2008,Colorado,4939456
