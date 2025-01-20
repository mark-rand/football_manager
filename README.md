# football_manager
Copy of Kevin Tomm's football manager from 1982

You can see the original code in [footmang.txt](footmang.txt)

## Cheats
An easy cheat - break into the code and type:
`6030 LET y(i)=20`
Then press continue - 20 energy for all players all the time
OR
`LET m = 1000000`
Gives you 1 million in the bank.

Map of the code

```Subroutines
260 - loads the football characters (graphics) into memory  
270 - 
280 - 
290 - goal
300 - game logic ? todo
350 - game logic ? todo
360 - in game thing? todo
400 - in game thing? todo
450 - some sort of in game thing? todo
460 - some sort of in game thing? todo
800 - save game (not a subroutine)
1000 - display money 
1010 - not enough money display
1020 - print league match details
1030 - enter to continue logic
1040 - 
1050 - top of team selection screen
1080 - 99 to continue menu
1090 - prints scores???
1100 - prints league
1120 - count how many players picked
1150 - unused!
1160 - ???
1170 - input a number
1180 - print the print option
2000 - main menu
2400 - logic for selling players
2540 - prints the heading of a player's stats
2550 - prints a player's stats
2800 - loan 
2900 - loan repayment
3000 - Prints manager stats
3200 - change skill level
4000 - works out if it is a cup game or league game
4100 - Introduction to week / calculates some stuff?
4240 - Team selection then Game then replay if needed
4500 - Prints round number of semi / final
4600 - 
4700 - 
5000 - runs the match
5200 - prints out the fa cup details
6000 - works out the team stats before a game
6500 - not sure - maybe prints out team stats
7000 - not sure - something about the goals for each team...
7500 - calculates scores of other matches - not quite sure how it works - does it actually just randomly allocate the matches each time?
7710 - calculates the league table
7805 - prints the league table 
8000 - calculates and prints the weekly bills
8100 - end of season logic
8500 - promotion logic
8600 - relegaton logic
8700 - transfer market
8785 - refused bid logic, increases price by 1/5th
8800 - initialises a bunch of variables
8900 - Starts with a weird loop then reads in team name, level and team colours from user
9000 - Loads the footballer names into an array p$
9400 - Change team names
9500 - Change player names
```
Variables
```a$() - Just an array of labels defined at line 9155
p$() - the footballer names
l$() - Array of level labels
m$ - manager name
t$ - the teams
u$ - this is the team number in order of the league (basically the league table)
y$ - temporary holder for chosen team to swap it with the 64th place team

b() - goals for?
c() - goals against?
c is the round of the cup
z() - team points

fa - set to 1 if out of the fa cup
lc - 1 for fa cup or 2 for league match
lt - the league offset of the team e.g. second division would set it to 16
d1 - current division from 4 to 1
ml - league match counter / number
p() - whether a player is in the squad or not = 0 for not in squad, 1 for in squad
r1 - player for sale?
t1 - chosen team number
s() - scores in the matches 
tco - team colour
v() - value of player
x9 - gate receipts
u() - I think this might be the matches?```

p = count of players picked
p1 = count of players available
