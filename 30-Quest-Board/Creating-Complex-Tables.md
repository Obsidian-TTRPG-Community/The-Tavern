---
attribution: jethoof
creation: 2023-05-06
modified: 2023-05-13
type: guide
---

# Crafting Complex Tables

Creating a random tables are really fun and helps in creating various situations from table top games to just writing inspirations. I have been using Dice Roller for both ways and here are some of the things I have found out.

## Tables in Tables  in Tables 
> [!tldr] 
> You can nest table results in tables and so on to create very complex generator.
^tldr1

You can create very complex tables with Dice Roller and here I will share something very simple with examples. In a typcial setting you would be looking for something like this:


> [!example]- Example Table Output Sentence
> [creature] is [height] and [physical trait] and is interested in [modifier] [motivation] and [modifier] [motivation] from the players. 
^example1

Each of the [field] is something you can create a table and you can test each of the setups. I use header 6 for tables and always include block (^) with table[#] for accessibility and consistency. 
###### Table 1 - 1d6 Table 

| dice: 1d6 | Result   |
| --------- | -------- |
| 1         | Option 1 |
| 2-3       | Option 2 |
| 4-5       | Option 3 |
| 6         | Option 4 |
^table1

The above table has 15% rolling option 1 and 4 while 30% for option 2 and 3. 

> [!example]- Table Output at Work
> `dice:[[Creating-Complex-Tables#^table1]]` and `dice:[[Creating-Complex-Tables#^table1]]` can happen.
^example2

This works for one set of topics but what if we can go deeper? We can add the tables within the table.

###### Table 2 - 1d4 Table 

| dice:1d4 | Result                                                 |
| -------- | ------------------------------------------------------ |
| 1        | `dice:[[Creating-Complex-Tables#^table1]]` |
| 2-3      | Option 5                                               |
| 4        | Option 6                                               |
^table2

> [!example]- Table within Tables, Results
> `dice:[[Creating-Complex-Tables#^table2]]` can happen. 
> 
^example3

You can see now the option 5 is 50% and option 6 is 25% while Option 1-4 is now lot lower because it's nested within the 25%. If you make tables that are basic building blocks you can combine into a complex one. Yes probability can be daunting but you don't have to think about it with this structure, the bigger the range, the greater the probability. The more nested it is, the less likely it would happen. I hope (but that's never really the case is it?)

###### Table 3 - Location

 | Location                                                                                         |
 | ------------------------------------------------------------------------------------------------ |
 | `dice:[[Creating-Complex-Tables#^table4]]` Tavern                                                |
 | `dice:[[Creating-Complex-Tables#^table4]]` Market                                                |
 | `dice:[[Creating-Complex-Tables#^table4]]` Dungeon                                               |
 | `dice:[[Creating-Complex-Tables#^table4]]` Forest                                                |
 | `dice:[[Creating-Complex-Tables#^table5]]`  and  `dice:[[Creating-Complex-Tables#^table6]]` home |
^table3

###### Table 4 - Senses

| Senses |
| ------ |
| `dice:[[Creating-Complex-Tables#^table6]]`     |
| `dice:[[Creating-Complex-Tables#^table5]]`    |
| smelly  |
| salty  |
| rough  |

^table4

###### Table 5 - Senses, Hear

| dice: 1d5 | Result |
| --------- | ------ |
| 1-2       | silent |
| 3-5       | loud   |

^table5

###### Table 6 - Senses, See

| dice: d% | Result       |
| -------- | ------------ |
| 1-60     | brightly lit |
| 61-100   | dim          |

^table6

Now you can roll Table 3 to get a result `dice:[[Creating-Complex-Tables#^table3]]` and you can full out the entire Table 4 with other tables to generate more specific outcomes as you can see in Table 3 it would give `dim and loud home` if it rolls the home location.

One thing to note, if you want to make a table with fair chance for all the options, you can make tables like 3 and 4. If you want to give some weight to certain rolls, include the "**dice: xdy**" column to create a range, I recommend using percentile die (`dice: d%`). 

## XY table 


> [!tldr] XY Table
> XY table option gives you a nice visualization to view, however it cannot be nested in tables.
^tldr2

Sometimes you want to create a matrix table with various results based on rolling two dice and many of the 2d20 systems, 2d6 systems uses these tables quite frequently. Dice Roller has a function to roll these tables with some caveats and the biggest benefit to this is how easy it is to view the table in a matrix format than a single table for every condition.

######  Table 7 - Alignment Table

| Result | 1              | 2            | 3            |
| ------ | -------------- | ------------ | ------------ |
| 1      | Lawful Good    | Neutral Good | Chaotic Good |
| 2      | Lawful Neutral | True Neutral | Chaotic Neutral              |
| 3      | Lawful Evil    | Neutral Evil | Chaotic Evil |
^table7

You can make such table and roll it using `dice:[[Creating-Complex-Tables#^table7]]|xy`. This table gives the same effect as if you put all the alignments in a single column. The benefit is better interface for your eyes and don't have to have long scrolling of table list. The downside of this format is you cannot nest this table in another table because currently the Dice Roller cannot parse this in a table.

###### Table 8 - dice roller cannot parse | within tables.

| table                                                     |
| --------------------------------------------------------- |
| `dice:[[Creating-Complex-Tables#^table7]]|xy` |
^table8

So for now xy method is good for rolls for a table that has fair chance for each of the outcomes that you want to have a quick visual uptake. 