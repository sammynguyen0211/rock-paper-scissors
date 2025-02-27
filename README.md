# rock-paper-scissors

import random

while True:
    print("===================")
    print("Rock Paper Scissors")
    print("===================")
    print("1) ✊")
    print("2) ✋")
    print("3) ✌️")
    pick = int(input("Pick a number: "))
    print("")
    
    if pick == 1:
        print("You Choose: ✊")
    elif pick == 2:
        print("You Choose: ✋")
    elif pick == 3:
        print("You Choose: ✌️")
    
    computer = random.randint(1,3)
    if computer == 1:
        print("Computer: ✊")
    elif computer == 2:
        print("Computer: ✋")
    elif computer == 3:
        print("Computer: ✌️")
    
    # Fixed win condition logic
    if (pick == 1 and computer == 3) or (pick == 2 and computer == 1) or (pick == 3 and computer == 2):
        print("You win!")
    elif pick == computer:
        print("Try again!")
    else:
        print("You lose!")
    
    play_again = input("Do you want to play again? (yes/no): ").lower()
    if play_again == "no":  # Fixed condition here
        print("Thanks for playing! Goodbye!")
        break  # Exit the loop
