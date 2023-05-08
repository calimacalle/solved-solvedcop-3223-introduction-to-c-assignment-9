Download Link: https://assignmentchef.com/product/solved-solvedcop-3223-introduction-to-c-assignment-9
<br>



1. Togive students practice in using arrays.

2. Togive students practice reading from files and writing to files.

The Problem: Automated Payroll

Many companies have a system where employees clock in andclock out to determine how much time they work each week. Since these recordsare already automatically stored in files on companies’ computers, it onlymakes sense to use these files to help calculate how much each employee shouldget paid. In order to determine how much an employee gets paid each week, youneed to know the following two pieces of information:

1) Thenumber of hours they worked in a week

2) Theirhourly pay rate

If an employee works 40 or less hours a week, then theysimply get paid the number of hours they worked times their hourly pay rate. Ifan employee works more than 40 hours, then they get paid an extra 50% of theirregular pay for the hours over 40 they worked. (For example, if an employee’spay rate is $10/hour and the employee works 50 hours, then he/she would getpaid $550, because he/she gets $10×50 = 500 normally, plus an extra .5x(10hr)x($10/hr) = $50 for his/her overtime.

You are to write a program that reads in the raw time datafrom the file “clock.txt”, processes the payroll and outputs thefinal results to the file “payroll.txt”. The input file will consistof all employee data for 10 weeks. Your output file will have summaries foreach week `as well as overall summaries for each employee. You are guaranteedthat the file will contain data for no more than 20 employees.

Format of clock.txt

The first line of the file will contain a single positiveinteger, n, in between 1 and 20,inclusive, which represents the number of employees at the company. Theseemployees will be numbered 0 through n– 1. The next n lines of the filewill each contain a single positive real number representing the hourly payrate for the corresponding employee. (Namely, the first line in this setcontains the pay rate for employee 0, the second line contains the pay rate foremployee 1, etc.). The next line will contain an integer w indicating how manyweeks of data will follow. The rest ofthe file will contain w sets of data. Each set of datarepresents the data for that particular week. The first line of each set ofdata will contain a single positive integer k,representing the number of employee records for the week. (Note: a singleemployee record denotes one instance of an employee clocking in and clockingout.) The following k lines willcontain one employee record each. Each employee record will have the followingformat:

Emp# HrIn MinIn HrOut MinOut

All five of these values will be integers. The firstinteger, Emp#,represents the employee number and will always be in between 0 and n – 1, inclusive. The second integer, HrIn,represents the hours (in military time) that the given employee clocked in towork. This value is guaranteed to be in between 0 and 23, inclusive. The thirdinteger, MinIn,represents the minutes (in military time) that the given employee clocked in towork. This value is guaranteed to be in between 0 and 59, inclusive. The lasttwo values, HrOut and MinOut, represent the hours andminutes respectively (in military time), that the given employee clocked out ofwork. You are guaranteed that this second time occurs later in the day than thefirst. (Thus, no employee EVER works through midnight.) Thus, the followingline:

3 8 0 16 30

means that employee number 3 worked from 8am to 4:30pm, fora total of 8.5 hours.

Format of payroll.txt

The first line of the output file will contain thefollowing

Number of employees: n

where n is thenumber of employees in the company. The second line will be a printout of thenumber of weeks of data in the format:

Number of weeks: w

The third line will be blank. Following that will be wsets of data, one for each of the w weeks in the input file. Eachcorresponding output data set will contain exactly n+2 lines. The first two lines will be as follows:

Week # EmpIDHours Pay

Substitute the corresponding week (1 through 10) for #, andseparate each heading on the second line with a tab. In the following n lines, list the appropriate data foremployees 0 through n-1, in order,separated by tabs. The second value will be the total number of hours theyworked in the week, printed to two decimal places, and the last value will betheir pay for the week, printed to two decimal places.

Following the w sets of data, after a blank line,list the totals for each employee. The first two lines for this last set ofdata should be as follows:

Total EmpIDHours Pay

Then, list the corresponding information in the same formatas the data sets for each individual week for the w week period.

Example Input and Output Files

Sample clock.txt

2

5.50

10.00

3

2

110 30 1330

0 70 16 30

4

09 0 1430

17 0 23 0

1 9 0 22 0

1 7 20 23 20

3

010 0 15 0

18 0 12 0

0 9 30 11 30

Sample Output – payroll.txt

Number of employees: 2Number of weeks: 3

Wk1

EmpID HoursPay

09.50 52.25

13.00 30.00

Wk2

EmpID HoursPay

014.50 79.75

142.00 410.00

Wk3

EmpID HoursPay

04.00 22.00

12.00 20.00

Total

EmpID HoursPay

028.00 154.00

147.00 460.00

Grading Notes

In order to receive full credit, not only does your programhave to work properly, but you must do the following:

1) Usemultiple functions (at least 2 functions other than main)

2) Defineconstants for appropriate values (you need to figure out what these are)

Input Specification

Assume that the input file that we use for testing adheresto all the specifications described above. (In essence, you do not have toerror check the input file at all.)

Output Specification

Your output file should follow the format describedabove.

Deliverables

Your assignment should besubmitted via Webcourses by the deadline. No assignments will be accepted viaemail. Your submission should include asingle .c file called payroll.c. Remember that your program will begraded using DevC++ , so be sure thatyour submitted code runs correctly in this IDE.If you do not have DevC++ on your personal machine, you may use acomputer in any lab to test your code.