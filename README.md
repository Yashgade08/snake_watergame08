# snake_watergame08
import random

def determine_winner(user_choice,computer_choice):
    if user_choice==computer_choice :
        return "its a tie"
    elif ((user_choice=="snake" and computer_choice=="water") or (user_choice=="water" and computer_choice=="gun") or (user_choice=="gun" and computer_choice=="snake")):
        return "you are win"
    else:
        return "computer win"

def play_game() :
    choices=['snake','water','gun']
    user_choice=input("enter your choice (snake , water ,gun) : ")
    if user_choice not in choices:
        print("invalid choice")
        return
    computer_choice=random.choice(choices)
    print(f"computer choise : {computer_choice}")
    result=determine_winner(user_choice,computer_choice)
    print(result)
play_game()
