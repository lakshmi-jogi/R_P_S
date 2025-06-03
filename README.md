# R_P_S
import random
def comp_ch():
    ch=["rock","paper","scissors"]
    return random.choice(ch)
def user_ch():
    ch=input("Enter your Choice[rock,paper,scissors]:").lower()
    while ch not in ["rock","paper","scissors"]:
        print("Invalid Input")
        ch=input("Enter your Choice:").lower()
    return ch
def win(user,comp):
    if user==comp:
        return "Tie"
    elif((user=="rock" and comp=="scissors") or (user=="paper" and comp=="rock") or (user=="scissors" and comp=="paper")):
        return "You Win"
    else:
        return "Computer Wins"
def play():
    print("Rock-Paper-Scissors Game")
    user=user_ch()
    comp=comp_ch()
    winner=win(user,comp)
    print(f"You Chose:{user}")
    print(f"Computer Chose:{comp}")
    print(winner)
play()
