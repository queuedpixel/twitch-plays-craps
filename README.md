# Twitch Plays Craps

Craps Table Played in Twitch Stream

## Player Guide

This guide will teach you how to play craps via Twitch chat.
If you're unfamiliar with craps, start with the [Craps Basics from Wizard of Odds](https://wizardofodds.com/games/craps/basics/).

### Under Development

This game is under development and not every possible craps bet is available right now.
Keep checking back to discover new bets and features as they get added!

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

* `pass` - Pass
* `pass-odds` - Pass Odds
* `dpass` - Don't Pass
* `dpass-odds` - Don't Pass Odds
* `field` - Field; 2 pays 2 to 1, 12 pays 3 to 1

If you wish to make a bet for the largest possible amount, use `max` instead of an amount when placing a bet.

You can increase or decrease a bet by issuing the `!bet` command again with a different amount.
You can remove a bet by using `0` as the amount.
Note that not every bet allows you to increase, decrease, or remove it at any time.

You may only use whole numbers for bet amounts.
However, your balance tracks fractional amounts since some bets pay out in fractional amounts.

The maximum odds is 100x.

Players may only place a bet if the banker has enough money to pay out the largest possible win for that bet, along with all other bets.
To prevent one player from monopolizing all of the banker's money, bets are limited to a maximum payout which is less than or equal to 1% of the banker's balance.
You are permitted to make a bet of 1, even if the largest possible win for that bet exceeds the maximum payout,
provided that the banker has a sufficient balance to pay out the largest possible win for that bet.
