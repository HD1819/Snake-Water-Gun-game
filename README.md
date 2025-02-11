# Snake-Water-Gun-game
It's a funny or time passing game.Here below provided the code of it.
import random
options = {"snack":1, "water":2, "gun":3}
print("choose any option from given option:", options)
user_choice = input("Enter your choice(snack, water, gun):").lower()
if user_choice not in options:
    print("Invalid choice! Please choose from snack, water, or gun.")
else:
    computer_choice = random.choice(list(options.keys()))
    print(f"you choose: {user_choice}")
    print(f"computer choose: {computer_choice}\n")

    if user_choice == computer_choice:
        print("It's a tie!")
    elif(user_choice == "snack" and computer_choice == "water") or \
        (user_choice == "water" and computer_choice == "gun") or \
        (user_choice == "gun" and computer_choice == "snack"):
        print("You win!")
    else:
        print("Computer wins!") 
