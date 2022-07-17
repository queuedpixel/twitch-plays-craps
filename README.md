# Twitch Plays Craps

Craps Table Played in Twitch Stream

## Player Guide

This guide will teach you how to play craps via Twitch chat.
If you're unfamiliar with craps, start with the [Craps Basics from Wizard of Odds](https://wizardofodds.com/games/craps/basics/).

### Under Development

This game is under development and not every bet is available right now.
Keep checking back to discover new features as they get added!

### Play Overview

Place bets using the `!bet` command.
Example: `!bet pass 1`

The game will automatically roll the dice a short while after the last bet is placed,
and will continue to roll the dice as long as there are bets remaining or the table has a point.

Players serve as the banker for the craps table.
Bets that are won are paid out by the banker and bets that are lost are paid to the banker.

You can serve as the banker using the `!banker` command.
If we already have a banker, you'll be placed into a queue to become the banker after the next seven out.
You can stop serving as the banker using the `!banker-stop` command.
You cannot bet while you are the banker.

Players begin with a starting balance of 10,000.00.
Players below the starting balance gain 1.00 on every roll.

### Command Guide

* `!help` - Show a link to this guide.
* `!banker` - Serve as the banker.
* `!banker-stop` - Stop serving as the banker.
* `!bet [type] [amount]` - Place a bet of the specified type for the specified amount.

### Bet Guide

The following bets are currently available:

* `pass` - *Pass* Bet
* `pass-odds` - Odds for *Pass* Bet
* `dpass` - *Don't Pass* Bet
* `dpass-odds` - Odds for *Don't Pass* Bet
* `field` - *Field* Bet; 2 pays 2 to 1, 12 pays 3 to 1
* `come` - *Come* Bet
* `come-point [point]` - *Come* Bet for Specified Point; used to increase *Come* bet on the specified point
* `come-odds [point]` - Odds for *Come* Bet on Specified Point
* `dcome` - *Don't Come* Bet
* `dcome-point [point]` - *Don't Come* Bet for Specified Point; used to decrease *Don't Come* bet on the specified point
* `dcome-odds [point]` - Odds for *Don't Come* Bet on Specified Point
* `place [point]` - *Place* Bet on Specified Point
* `dplace [point]` - *Place to Lose* Bet on Specified Point
* `buy [point]` - *Buy* Bet on Specified Point
* `lay [point]` - *Lay* Bet on Specified Point
* `any-craps` - *Any Craps* Bet; pays 7.5 to 1
* `any-seven` - *Any Seven* Bet; pays 4 to 1
* `hard [point]` - *Hard Way* Bet on Specified Point; 4 and 10 pay 7 to 1, 6 and 8 pay 9 to 1
* `hop [die1] [die2]` - *Hop* Bet on the Specified Die Roll; **hard** rolls pay 33 to 1, **easy** rolls pay 16 to 1
* `all` - *All* Bet; pays 175 to 1 for rolling 2, 3, 4, 5, 6, 8, 9, 10, 11, 12 (in any order) before rolling 7
* `tall` - *Tall* Bet; pays 34 to 1 for rolling 8, 9, 10, 11, 12 (in any order) before rolling 7
* `small` - *Small* Bet; pays 34 to 1 for rolling 2, 3, 4, 5, 6 (in any order) before rolling 7
* `fire` - *Fire* Bet; pays based on the number of unique points made before seven out; 4 points pays 24 to 1, 5 points pays 249 to 1, 6 points pays 999 to 1

You can make a bet for the largest possible amount by using `max` instead of an amount when placing a bet.

You can increase or decrease a bet by issuing the `!bet` command again with a different amount.
You can remove a bet by using `0` as the amount.
However, not every bet allows you to increase, decrease, or remove it at all times.

You may only use whole numbers for bet amounts.
However, your balance tracks fractional amounts since some bets pay out in fractional amounts.

The maximum odds is 100x.

You may only place a bet if the banker has enough money to pay out the largest possible win for that bet, along with all other bets from all players.
To prevent one player from monopolizing all of the banker's money, bets are limited to a maximum payout which is less than or equal to 1% of the banker's balance.
You are permitted to make a bet of `1`, even if the largest possible win for that bet exceeds the maximum payout,
provided that the banker has a sufficient balance to pay out the largest possible win for that bet.

In a casino some of your bets are automatically turned off on a come-out roll, such as odds for *Come* bets.
This game does not do this for you.
If you want to turn bets off for the come-out, or at any other time, you must remove them manually.
