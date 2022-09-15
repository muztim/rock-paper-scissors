# rock-paper-scissors

rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

#Write your code below this line 👇
import random
#List of computer choices
list = [rock, paper, scissors]
#User play
user_choice = int(input("Choose 0 for Rock, 1 for Paper or 2 for Scissors \n"))
if user_choice < 0 or user_choice >= 3:
  print("Invalid entry, You lose") 
else:
  print(list[user_choice])
#random computer choice
  comp_choice = random.randint(0,2)
  
  print("The computer chooses")
  print(list[comp_choice])
 
  if comp_choice == 0 and user_choice == 2:
    print("You lose")
  elif user_choice == 0 and comp_choice == 2:
    print("You win")
  elif user_choice > comp_choice:
    print("You lose")
  elif user_choice == comp_choice:
    print("It's a draw")
