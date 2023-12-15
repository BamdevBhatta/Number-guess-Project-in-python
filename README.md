import random
top_of_range = input("Type Range of  Number You want to find out: ")

if top_of_range.isdigit():
    top_of_range = int(top_of_range)


    if top_of_range <= 0:
        print("Please type a number larger then 0 next time")
        quit()


else:
    print("Type a number next time ")





random_number = random.randint(0,top_of_range)
guesses = 0


#print(random_number)
while True:
    guesses += 1
    user_guess = input(f"Please Guess a number between 0 to {top_of_range}: ")
    if user_guess.isdigit():
        user_guess = int(user_guess)

    else:
        print("Please try a number next time.")
        continue

    #print("After Continue")
    if user_guess == random_number:
        print("You got it")
        break
    elif  user_guess > random_number:
        print("You were below the number")
    else:
        print("You were above the number!")
        


print("You got it in ", guesses, " guesses")
print("42:53")
