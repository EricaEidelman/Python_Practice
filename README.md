# Python Practice

## Overview
This repository is a commpilation of several projects in the Codecademy Python course to practice working with functions, strings, lists, and dictionaries.

## Reggie's Linear Regression
This project uses functions to find a linear regression line (y = mx + b) for a dataset of multiple points. After creating a function which calculates the total error of a line through the datapoints, the program iterates through a list of m and b values to find which result in the smallest error.

```
datapoints = [(1, 2), (2, 0), (3, 4), (4, 4), (5, 3)]
smallest_error = float("inf")
best_m = 0
best_b = 0

for m in possible_ms:
    for b in possible_bs:
        error = calculate_all_error(m,b,datapoints)
        if error < smallest_error:
            best_m = m
            best_b = b
            smallest_error = error
            
print(best_m, best_b, smallest_error)
```

## Coded Correspondence
This project uses functions to decode encoded messages. One of the ciphers used is the Caesar cipher, in which each letter is offset by a predetermined amount. The function looks like the below, and a similar function can be used to encode messages:

```
def decoder(message, offset):
    new_message = ""
    punctuation = ".,?!' "
    alphabet = "abcdefghijklmnopqrstuvwxyz"
    for letter in message:
        if letter in punctuation:
            new_message += letter
        else:
            alphabet_location = alphabet.rfind(letter)
            letter = alphabet[(alphabet_location + offset) % 26]
            new_message += letter
    print(new_message)
```

## Abruptly Goblins
This project uses functions to help plan the best day for a game night depending on the largest player availability. After going through a list of players and their available days, the day with the most players available is selected and the players available that day are identified. Another function is then used to generate an email message inviting players to the game, as below. Similar functions are made to find the second best day and likewise send emails to those available that day.

```
def send_email(gamers_who_can_attend, day, game):
    for gamer in gamers_who_can_attend:
        print(form_email.format(name=gamer, day_of_week=day, game=game))
        
send_email(attending_game_night, game_night, "Abruptly Goblins!")
```
