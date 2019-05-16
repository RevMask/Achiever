# Fun category
This can be accessed via `d.help Fun` (please note the capital letter)

Reminder: commands are called with the prefix `d.`

## Commands in the Fun category:
  8ball, bin, coin, money, ouinon, quote, roll, roulette, rps, rpsls, sino, slots, yesno

### 8ball [question]
**Magic 8-Ball**

Will give you an answer to your important question. You can either think of a question while typing, or include it after the command. The magical oracle can read your mind if you just type.

Uses Supernatural APIs to access magical sources.

### Dice and Random Rolls
There are various commands for game rolls. They are:
  roll, bin, coin

**roll**
Rolls dice in standard dice notation. If you've ever played Dungeons & Dragons or other tabletop RPGs, you're probably very familiar with standard dice notation

Will return a random value based on the specified dice notation. The format is:

  `[n]d<s>[modifier]`
  
where _*n*_ is the number of dice (default 1), mandatory letter _*d*_ (no quotes), _*s*_ is the the number of sides, and an optional modifier, +, -, \*, /, and an integer

Sides can be any integer, or a special:
   c    coin toss (`d.roll dc` is the same as `d.coin`)
   b    binary (0, 1) (`d.roll db` is the same as `d.bin`)
   %    percent roll (same as d100 plus '%')
   y,n  yes/no result (`d.roll dy|dn` is the same as `d.yesno`)

Some examples are: d4 (4-sided die), 3d6 (3 x 6-sided dice), d% (random percentage), d100 (like % but without percent sign), 1d20+2 (20-sided die, adding 2).

