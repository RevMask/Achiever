# Fun category
This can be accessed via `d.help Fun` (please note the capital letter)

Reminder: commands are called with the prefix `d.`

## Commands in the Fun category:
  8ball, bin, coin, money, ouinon, quote, roll, roulette, rps, rpsls, save, sino, slots, yesno

### Dice and Random Rolls
There are various commands for game rolls. They are:\
    roll, bin, coin, save

**roll**  
Rolls dice in standard dice notation. If you've ever played Dungeons & Dragons or other tabletop RPGs, you're probably very familiar with standard dice notation.

Will return a random value based on the specified dice notation. The format is: `[n]d<s>[modifier]`\
where _*n*_ is the number of dice (default 1), mandatory letter _*d*_ (no quotes), _*s*_ is the the number of sides, and an optional modifier, +, -, \*, /, and an integer

Sides can be any integer, or a special:

|special|description |same as               |
|:-----:|:-----------|:---------------------|
|c      |coin toss   |`d.coin`              |
|b      |binary (0,1)|`d.bin`               |
|%      |percent roll|`d.roll d100` plus '%'|
|y,n    |yes/no      |`d.yesno`             |

Some examples are: d4 (4-sided die), 3d6 (3 x 6-sided dice), d% (random percentage), d100 (like % but without percent sign), 1d20+2 (20-sided die, adding 2).

There is a limit of 1024 sides and 1024 dice. We found out the hard way it can kill the bot!

**save <value> <roll>**  
Make a saving throw. These are in tabletop RPGs. You are trying to roll the *value* or higher. The *roll* must be in standard dice notation as shown above.

**bin**  
*aliases:* bin, binary, 01, 10  
Performs a binary roll. Returns an answer of 0 or 1. This is identical to `d.roll db`.

**coin**  
*aliases:* coin, toss, flip, headstails, heads, tails  
Performs a coin toss. Returns an answer of "heads" or "tails." This is identical to `d.roll dc`.

**yesno [question]**  
Answers yes or no to your question. The question is optional.  
This is identical to `d.roll dy` and `d.roll dn`.

**ouinon [question]**  
Recevez une réponse oui/non. The French version of `yesno`, answering in French. Can also take an optional question.

**sino [pregunta]**  
Recibe una respuesta de sí/no. The Spanish version of `yesno`, answering in Spanish. Can also take an optional question.

### Games, Etc.
**8ball [question]**  
**Magic 8-Ball**  
Will give you an answer to your important question. You can either think of a question while typing, or include it after the command. The magical oracle can read your mind if you just type.

Uses Supernatural APIs to access magical sources.

**quote [source]**  
Fun quotes from various sources. Can be used with or without a parameter. Defaults to quotes from "The Big Lebowski"  

|parameter                 |source             |
|:-------------------------|:------------------|
|*\<none>*                 |The Big Lebowski   |
|sw, starwars              |Star Wars (various)|
|rm, rickmorty, rick, morty|Rick & Morty       |
|mv, movie, movies         |Movies, various    |
|marvel, mcu               |Marvel movies      |

**roulette [bet] [wager=100]**  
*aliases:* roul, rou  
**Roulette**  
Based on American-style roulette. If no wager is given, the default 100 is used. The bets and their payouts are:  

|Name           |Description            |Payout |
|---------------|-----------------------|------:|
|red, r, rouge  |Any red number         |    1:1|
|black, k, noir |Any black number       |    1:1|
|low, low       |1-18                   |    1:1|
|high, hi       |19-36                  |    1:1|
|dozen1, dz1    |1-12                   |    2:1|
|dozen2, dz2    |13-24                  |    2:1|
|dozen3, dz3    |25-36                  |    2:1|
|column1, col1  |Any in column 1        |    2:1|
|column2, col2  |Any in column 2        |    2:1|
|column3, col3  |Any in column 3        |    2:1|
|basket         |0, 00, 2               |    6:1|
|topline        |0, 00, 1, 2, 3         |    6:1|
|*number*       |Straight (exact number)|   35:1|
|0, 00, zero    |Zero                   |   36:1|  

The columns are:  
*column 1:* 1, 4, 7, 10, 13, 16, 19, 22, 25, 28, 31, 34  
*column 2:* 2, 5, 8, 11, 14, 17, 20, 23, 26, 29, 32, 35  
*column 3:* 3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33, 36  

This does seem confusing, so here is a reminder:  
![American Roulette](https://github.com/RevMask/Achiever/blob/master/images/american-roulette-1200.png "American Roulette wheel and board")

**rps [rec|record]**  
**Rock Paper Scissors**  
Play against Achiever! It will ask you for your choice. It really is random, dudes. Trust me. You can see your win/loss/tie record with the optional argument.

Rock beats/destroys scissors. Paper beats/covers rock. Scissors beat/cut paper.

**rpsls [rec|record]**  
*aliases:* spock, r5  
Play Rock, Paper, Scissors. Lizard, Spock, the game created by Sam Kass and Karen Bryla. Achiever will ask you for your choice. Again, it's random. Honestly. You can see your win/loss/tie record with the optional argument.

Scissors cuts paper, paper covers rock, rock crushes lizard, lizard poisons Spock, Spock smashes scissors, scissors decapitate lizard, lizard eats paper, paper disproves Spock, Spock vaporizes rock, and as it always has, rock crushes scissors. *(Thanks, Dr. Cooper!)*


**slots [amount]**  
**Dude Slot Machine**  
I'm proud of this one. You specify your wager amount, and the bot will randomly spin the machine. Each time someone loses, it's added to the jackpot. Enter `d.slots` with no argument to see the current jackpot amount. The payouts are:  

|1         |2         |3         | Payout|
|:--------:|:--------:|:--------:|------:|
|Dude      |Dude      |Dude      |jackpot|
|bar       |bar       |bar       |   x250|
|bell      |bell      |bell/bar  |    x20|
|plum      |plum      |plum/bar  |    x15|
|orange    |orange    |orange/bar|    x10|
|lemon     |lemon     |lemon/bar |     x8|
|cherry    |cherry    |cherry    |     x7|
|cherry    |cherry    |*(any)*   |     x5|
|cherry    |*(any)*   |*(any)*   |     x2|

