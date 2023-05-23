# Snake_Water_Gun
This is my first python project. I have created this mini game in python during my python learning journey.

print("Welcome to Snake, Water, Gun Game !\nlets play ..")
print("Rules :\nif you choose 1(Water) and computer chooses 0(Snake) then computer will win\n"
      "if you choose 2(Gun) and computer chooses 1(Water) then computer will win\n"
      "if you choose 0(Snake) and computer chooses 2(Gun) then computer will win\n"
      "if you choose 0(Snake) and computer chooses 1(water) then you will win\n"
      "if you choose 1(Water) and computer chooses 2(Gun) then you will win\n"
      "if you choose 2(Gun) and computer chooses 0(Snake) then you will win\n"
      "if you and computer chooses same choice then game will draw\n")

import random
while True:

    comp = random.randint(0,2)
    user = int(input("kindly Choose 0 for Snake, 1 for Water and 2 for Gun :\n"))

    if user not in (0,1,2):
        print("Please enter a valid input\nPlay again:")
        break
    def check(comp,user):
        if (comp == 0 and user == 1):
            return -1
        if (comp == 1 and user == 2):
            return -1
        if (comp == 2 and user == 0):
            return -1
        if comp == user:
            return 0
        else:
            return 1

    print("You :",user)
    print("Computer :",comp)

    score = check(comp,user)
    if score == 0:
        print("Its a draw")
    elif score == -1:
        print("You lose")
    else:
        print("Congratulations! you won")
        break
