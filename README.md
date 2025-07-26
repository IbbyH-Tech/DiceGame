import random

print('This is a dice game!')

game = 1

while game == 1:  
    points = 15
    rolls = 0
   
    while points > 0:
        input("Press Enter to roll the dice...")

        dice = random.randint(2, 12)
        points -= 10
        rolls += 1

        if dice == 12:
            points += 20
        elif dice == 11:
            points += 17
        elif dice == 10:
            points += 15
        elif dice == 9:
            points += 13
        elif dice == 8:
            points += 11
        elif dice == 7:
            points += 10
        elif dice == 6:
            points += 7
        elif dice == 5:
            points += 5
        elif dice == 4:
            points += 3
        elif dice == 3:
            points += 2

        print("Dice roll:", dice)
        print("Points:", points)
        print("Number of rolls:", rolls)

        if points <= 0:
            print("Game over! You've run out of points.")

    play_again = input("Would you like to play again? (Type 'yes' to play again or type 'no' to quit): ")
    if play_again == 'yes':
        game = 1
    else:
        game = 0 
