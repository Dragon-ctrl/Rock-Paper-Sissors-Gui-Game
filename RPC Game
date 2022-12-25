from tkinter import *
from tkinter import ttk
from random import randint

# Create window and set title
root = Tk()
root.title("Rock, Paper, Scissors")

# Define global variables
user_choice = ""
bot_choice = ""
bot_score = 0
user_score = 0
result = ""
start_screen = True

# Define function for setting user choice
def set_user_choice(choice):
    global user_choice
    user_choice = choice

# Define function for generating bot choice
def set_bot_choice():
    global bot_choice
    bot_choice = randint(1,3)
    if bot_choice == 1:
        bot_choice = "rock"
    elif bot_choice == 2:
        bot_choice = "paper"
    elif bot_choice == 3:
        bot_choice = "scissors"

# Define function for comparing choices
def compare_choices():
    global user_choice
    global bot_choice
    global user_score
    global bot_score
    global result
    if user_choice == bot_choice:
        result = "It's a tie!"
    elif user_choice == "rock" and bot_choice == "paper":
        result = "Bot wins!"
        bot_score += 1
    elif user_choice == "rock" and bot_choice == "scissors":
        result = "User wins!"
        user_score += 1
    elif user_choice == "paper" and bot_choice == "rock":
        result = "User wins!"
        user_score += 1
    elif user_choice == "paper" and bot_choice == "scissors":
        result = "Bot wins!"
        bot_score += 1
    elif user_choice == "scissors" and bot_choice == "rock":
        result = "Bot wins!"
        bot_score += 1
    elif user_choice == "scissors" and bot_choice == "paper":
        result = "User wins!"
        user_score += 1

# Define function for playing the game
def play():
    global user_choice
    global bot_choice
    set_user_choice(choice.get())
    set_bot_choice()
    compare_choices()
    print("User chose: " + user_choice)
    print("Bot chose: " + bot_choice)
    print("User score: " + str(user_score))
    print("Bot score: " + str(bot_score))
    result_label.config(text=result)
    user_score_label.config(text="User Score: " + str(user_score))
    bot_score_label.config(text="Bot Score: " + str(bot_score))
    bot_choice_label.config(text="Bot Choice: " + bot_choice)

# Define function for starting the game
def start():
    global start_screen
    start_screen = False
    start_frame.pack_forget()
    frame.pack()

# Configure window and create frames
root.configure(background='#2196F3')
start_frame = Frame(root, bg='#2196F3', padx=20, pady=20)
frame = Frame(root, bg='#2196F3', padx=20, pady=20)

# Create start label
start_label = Label(start_frame, text="Let's Play Rock, Paper, Scissors!", font=('Gotham', 16), bg='#2196F3', fg='white')

# Create start button
start_button = Button(start_frame, text="Start", font=('Gotham', 16), command=start, bg='#2196F3', fg='white', activebackground='#BBDEFB', activeforeground='#2196F3')

# Create label for choice
label = Label(frame, text="Choose: ", font=('Gotham', 16), bg='#2196F3', fg='white')

# Create variable for user choice
choice = StringVar()

# Create radio buttons for choices
rock = Radiobutton(frame, text="Rock", font=('Gotham', 16), variable=choice, value="rock", bg='#2196F3', fg='white', indicatoron=0, selectcolor='#2196F3', relief="raised")
paper = Radiobutton(frame, text="Paper", font=('Gotham', 16), variable=choice, value="paper", bg='#2196F3', fg='white', indicatoron=0, selectcolor='#2196F3', relief="raised")
scissors = Radiobutton(frame, text="Scissors", font=('Gotham', 16), variable=choice, value="scissors", bg='#2196F3', fg='white', indicatoron=0, selectcolor='#2196F3', relief="raised")

# Create button for playing
button = Button(frame, text="Play", font=('Gotham', 16), command=play, bg='#2196F3', fg='white', activebackground='#BBDEFB', activeforeground='#2196F3')

# Create result label
result_label = Label(frame, text="", font=('Gotham', 16), bg='#2196F3', fg='white')

# Create score labels
user_score_label = Label(frame, text="User Score: 0", font=('Gotham', 16), bg='#2196F3', fg='white')
bot_score_label = Label(frame, text="Bot Score: 0", font=('Gotham', 16), bg='#2196F3', fg='white')
bot_choice_label = Label(frame, text="Bot Choice: ", font=('Gotham', 16), bg='#2196F3', fg='white')

# Pack widgets
start_label.pack()
start_button.pack()
label.pack()
rock.pack()
paper.pack()
scissors.pack()
button.pack()
result_label.pack()
user_score_label.pack()
bot_score_label.pack()
bot_choice_label.pack()

if start_screen:
    start_frame.pack()
else:
    frame.pack()

# Run main loop
root.mainloop()
