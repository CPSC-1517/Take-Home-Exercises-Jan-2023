# CPSC1517-1222 Exercise 3

> This exercise is not related to the previous exercises and covers topics on Razor Pages

## Objective

Upon completion of this exercise, you will have demonstrated the ability to:
- Modify a Razor Page to display an image
- Create and code a C# class to model a Person
- Create and code a Razor Page to process a HTML form submission
- Create and code a Razor Page to handle multiple submit buttons
- Create and code a Razor Page to display a collection of objects

## Problem Description

You are the Computer Software Developer co-op student for the King of England where you have been given the task to create a new ASP.NET Core Web App with the following pages:

- A page with an fixed-size image of yourself and a description of yourself for the King to know you better. 
- A page that allows the King to know the age, chinese zodic, and astrological sign of a person by entering the person's name and date of birth. For succession planning the King would like also to able to determine the age of a person on a specific date.
- A page to that reads data from the provided `RoyalFamily.json` file and display the family name and the name, date of birth, current age, chinese zodic animal, and astrological sign of each person in the family.
- A page that allows the King to assign members to teams for a given list of names and the number of teams.

The Chinese Zodic animal of a person can be determine by looking up the following table.

| Year of birth % 12 | Animal |
| --- | --- |
| 0 | Monkey |
| 1 | Rooster |
| 2 | Dog |
| 3 | Pig |
| 4 | Rat |
| 5 | Ox |
| 6 | Tiger |
| 7 | Rabbit |
| 8 | Dragon |
| 9 | Snake |
| 10 | Horse |
| 11| Sheep |

The Astrological sign of a person can be determine by looking up the following table.

| Birth Dates | Sign |
| --- | --- |
| March 21 - April 19 | Aries |
| April 20 - May 20 | Taurus |
| May 21 - June 21 | Gemini |
| June 22 - July 22 | Cancer |
| July 23 - August 22 | Leo |
| August 23 - September 22 | Virgo |
| September 23 - October 22 | Libra |
| October 23 - November 22 | Scorpio |
| November 23 - December 21 | Sagittarius |
| December 22 - January 19 | Capricorn |
| January 20 - February 18 | Aquarius |
| February 19 - March 20 | Pisces |

## Requirements
1. Create a new ASP.NET Core Web App named `CPSC1517-Ex03-YourName`
1. Modify the `Index.cshtml` file display an image of you and a one sentence description of yourself. 
1. Add a new folder to your project named `Models`
1. In the `Models` folder, add a new C# class named `Person`.
1. Modify the `Person` class to add public properties for the `Name` and `DateOfBirth`
1. Modify the `Person` class to add a constructor to set `Name` to your full name and the `DateOfBirth` to your date of birth.
1. Modify the `Person` class and add a public property (read-only) that returns the current age of the person as of the current date.
1. Modify the `Person` class and add a instance-level method that is passed a `DateTime` parameter and returns the current age of the person as of the `DateTime` parameter value.
1. Modify the `Person` class and add a instance-level method that returns the Chinese Zodiac animal of the person as described in table 1.
1. Modify the `Person` class and add a instance-level method that returns the the Astrological Sign of the person as described in table 2.
1. Add a new Razor Page named `PersonInfo`. Write code to create an HTML form with form fields that allows the user to enter the `Name`, `DateOfBirth`, and `AgeOnDate` of a person. Add a submit button that when clicked will display the current age, Chinese Zodiac name, and Astrological Sign of the person. Add another button when clicked will display the age of the person using the age of date form field value. Add another button when clicked will clear the form fields.
Add server-side validation code to ensure the Name is not blank and contains at minimum 5 characters in length and the birth date is not in the future.
1. Add a new Razor Page named `RoyalFamilyList`. Write code to read from the `RoyalFamily.json` file and and the name, date of birth, current age, chinese zodic animal, and astrological sign of each person in the family in an HTML table.
1. Add a new Razor Page named `CreateTeams`. Write code to create an HTML form with a `textarea` field for entering a list of names and a `select` field that selecting the number of teams from 2 to 10. Add a submit button that when clicked will split the list of names into a sub-list of names then display the team number and the name for each member of the team. For example, if there are 10 names in list and we want to create 3 teams then there will be a maximum of 4 members per team and the first team will have 4 members and the last two teams will have 3 members each.
The members of each team must be randomly selected. You are not required to sort the names of each member of a team.
You are expected to do your own research on how to implement the logic to solve this problem. (Hint 1: each line in a textarea form field is separated by a newline character.) (Hint 2: the calculated maximum number members per team must be rounded up to the nearest integer value.)

1. Edit the Shared `_Layout.cshtml` file and add navigation links to the three pages you added.
1. OPTIONAL CHALLENGE: display in image instead of text for the Chinese Zodiac animal and Astrological Sign of person in both the `PersonInfo` and `RoyalFamilyList`
----

### Samples

## Index Page

![Home Page](./images/IndexRazorPage.png)

## PersonInfo Page

![PersonInfo Page](./images/PersonInfo.png)

## PersonInfo Page - Current Age

![PersonInfo Page](./images/PersonInfo_CurrentAgeResult.png)

## PersonInfo Page - Age On

![PersonInfo Page](./images/PersonInfo_AgeOneResult.png)

## Royal Family Page

![Royal Family](./images/RoyalFamilyListRazorPage.png)

## Create Team Input/Output Page

![InputPage](./images/CreateTeamsRazorPage.png)

![Output](./images/CreateTeamsRazorPageResult.png)

## Person Class Diagram

![Classdiagram](./images/PersonClassDiagram.png)

## Evaluation

> ***NOTE:** Your code **must** compile. Solutions that do not compile will receive an automatic mark of zero (0).*
> 
> If you are unable to get a portion of the assignment to compile or work, you should:
> - Comment out the  portion of code
> - Identify the reason for the commented portion (such *as does not compile* or *does not work cause an abort*)

Your assignment will be marked based upon the following weights. See the [general rubric](../../README.md#generalized-marking-rubric) for details.


| Earning | Weight | Deliverable/Requirement | Comment |
| ---- | --------- | ------- | ------------- |
|   | 1 | `Index.cshtml` |    |
|   | 3 | Person.cs |    |
|   | 5 | `PersonInfo.cshtml` and `PersonInfo.cshtml.cs` |   |
|   | 2 | `RoyalFamilyList.cshtml` and `RoyalFamilyList.cshtml.cs` |    |
|   | 4 | `CreateTeams.cshtml` and `CreateTeams.cshtml.cs` |   |
|  | -3 | Other concerns and penalities (Missing links to each page in layout file, commits reflect incremental development) max -3 |   |
| ---- | ----- | --------- |  ------ |
|   | **15** | **Total Weight** | ------ |
| ---- | ----- | --------- | ------ |


----

[Return to exercises](../../README.md)

