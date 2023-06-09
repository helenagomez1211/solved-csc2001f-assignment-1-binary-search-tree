Download Link: https://assignmentchef.com/product/solved-csc2001f-assignment-1-binary-search-tree
<br>
The goal of this assignment is to compare the Binary Search Tree with a traditional unsorted array data structure, both implemented in Java, using a real-world application to read in and provide access to dam water level data.

DatasetThe attached historical dam water level data file was obtained from the Code for South Africa Data Portal at https://data.code4sa.org/Government/Dam-Levels-Individual-Nov2015-Mar2016/yqb8-aumt/data

Load the file into LibreOffice/OpenOffice/MS-Excel to see what the data looks like. Take note that the first line has headings and needs to be ignored by your code. Every subsequent line represents a single data item.

In your application, you MUST write your own code to read in the CSV file. You may not use a CSV library. Your data structure items must each store at least the following 3 values extracted from the CSV file:

“Dam Name”“FSC 1,000,000m³ (million m³)” (which we will call “FSC”)“20160307 (percent full)” (which we will call “dam level”)Part 1Write an application DamArrayApp to read in the attached CSV file and store the data items within a traditional array (a single array of objects). There are 211 data items – you may use a fixed-size array or try to determine the size programmatically. Do not use a LinkedList, ArrayList or other advanced data structure.

Include the following methods in your code:

printDam (damName) – to print out the dam name, FSC and dam level for the first matching dam name found; or “Dam not found” if there is no match.printAllDams () – to print out the dam name, FSC and dam level for every dam, in any orderYou should be able to invoke your application using commands such as

java DamArrayApp “Pella Dam”

to print details for “Pella Dam”, or

java DamArrayApp

to print all dam details. You may use quotes in your parameters or not – it is up to you.

Test your application with 3 known dam names, one unknown dam name and without any parameters. Use output redirection in Unix to save the output in each case to different files.

Part 2Add additional code to your solution to Part 1 to discretely count the number of comparison operations (&lt;, &gt;, =) you are performing in the code. Only count where you are comparing the names of dams. This is called instrumentation. There are 3 basic steps.

First, create a variable/object (e.g., opCount=0) somewhere in your code to track the counter; maybe use an instance variable in the data structure class.

Secondly, wherever there is an operation you want to count, increment the counter (opCount++). For example:

opCount++; // instrumentation

if (queryDam == theDam)…

Finally, report the value of the counter before the program terminates. Maybe add a method to write the value to a file before the program terminates.

Test your application with 3 known dam names, one unknown dam name and without any parameters. Take note of the operation count in each case.

Part 3Write an application DamBSTApp to perform the same tasks as Part 1, but using a Binary Search Tree (BST) instead of an array.

Your BST implementation can be created from scratch or re-used from anywhere. You may NOT replace the BST with a different data structure.

Once again, test your application with 3 known dam names, one unknown dam name and without any parameters. Use output redirection in Unix to save the output in each case to different files.

Part 4Instrument your DamBSTApp code just as you did in Part 2.

Test your application with 3 known dam names, one unknown dam name and without any parameters. Take note of the operation count in each case.

Part 5Conduct an experiment with DamArrayApp and DamBSTApp to demonstrate the speed difference for searching between a BST and a traditional array.

You want to vary the size of the dataset (n) and measure the number of comparison operations in the best/average/worst case for every value of n (from 1-211). For each value of n:

Create a subset of the sample data (hint: use the Unix head command).Run both instrumented applications for every dam name in the subset of the data file. Store all operation count values.Determine the minimum (best case), maximum (worst case) and average of these count values.It is recommended that you use Unix or Python scripts to automate this process.

ReportWrite a report (of up to 6 pages) that includes the following:

What your OO design is: what classes you created and how they interact.What the goal of the experiment is and how you executed the experiment.What test values you used in the trial runs (Part 2 and Part 4) and what the operations counts were in each case. Only show the first 10 and last 10 lines for the trial run where you invoke printAllDams ().What your final results are (use one or more graphs), showing best, average and worst cases for both applications. Discuss what the results mean.A statement of what you included in your application(s) that constitutes creativity – how you went beyond the basic requirements of the assignment.Summary statistics from your use of git to demonstrate usage. Print out the first 10 lines and last 10 lines from “git log” , with line numbers added. You can use a Unix command such as:git log | (ln=0; while read l; do echo $ln: $l; ln=$((ln+1)); done) | (head -10; echo …; tail -10)

Dev requirementsAs a software developer, you are required to make appropriate use of the following tools:

git, for source code managementjavadoc, for documentation generationmake, for automation of compilation and documentation generation