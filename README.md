# programs
Problem: The “witchy” programmer
Somewhere far far away, there is a village which is controlled by a dark and cunning witch. Coincidentally, this witch is also a die-hard programmer.
The witch has power to control death and life of the villager. The witch will kill a number of villagers each year.
Since the witch is a die hard programmer, she follows a specific rule to decide the number of villagers she should kill each year.
On the 1st year she kills 1 villager
On the 2nd year she kills 1 + 1 = 2 villagers
On the 3rd year she kills 1 + 1 + 2 = 4 villagers
On the 4th year she kills 1 + 1 + 2 + 3 = 7 villagers
On the 5th year she kills 1 + 1 + 2 + 3 + 5 = 12 villagers
And so on…

The villagers are furious with the witch and want to get rid of her and there is one way to get rid of her.
The witch will only leave if there is a brave programmer in the villager who can create a program to solve this problem:
If given two people whose age of death and year of death are known, find the average number of people the witch killed on year of birth of those people
Example:
Given:
Person A: Age of death = 10, Year of Death = 12
Person B: Age of death = 13, Year of Death = 17
Answer:
Person A born on Year = 12 – 10 = 2, number of people killed on year 2 is 2.
Person B born on Year = 17 – 13 = 4, number of people killed on year 4 is 7.
So the average is (7 + 2)/2 = 4.5
If you give invalid data (i.e. negative age) the program should return -1.
So, if someone can create a program to solve the problem, the witch will leave and the killing will stop.
There was one programmer who was able to solve the problem, but the witch did not like the code because the code was messy and made her angry.
She then proceeded to kill the programmer. Now the villagers know that they also need to make the code clean and structured. Now you are asked by the villagers to do another attempt in solving this problem.

Solution:
In this program, we are passing list of persons, which returns average number of people killed on the born year of those people.

1) Check the persons, no negative age allowed. born year can not be greater than age of death.
2) Find maximum year, upto which we need to find killed people count.
3) Find killed people for all the years upto maximum year.
4) Find people killed for the born year of given persons.
5) Calculate average of killed people.

How to run?
Run the WitchyProgrammerApplication as Java Application
API to call
	Method: POST
	URL: localhost:8080/prgorammer/
	Header: Content-Type: application/json
	Body:
		[
			{
				"ageOfDeath":10,
				"yearOfDeath":12
			},
			{
				"ageOfDeath":13,
				"yearOfDeath":17
			}
		]
Time Complexity: O(n+k)
Space Complexity: O(n+k)
Where 'n' is number of person and 'k' is max number of years found

Calculation for given request:
1 = 0+1 = 1
1+[1] = 1+1 = 2
1+1+[2] = 2+2 =  4
1+1+2+[3] = 3+4 = 7

Person 1: 12-10=2 > Number of people killed = 2
Person 2: 17-13=4 > Number of people killed = 7

Average of 2 and 7 = 4.5