import random


def start_game():

    print("Hey there want to play a guessing game?  ")
    answer = random.randrange(1, 10)
    tries = 0
    try:
        guess = int(input("Pick a number between 1 and 10  "))
    except ValueError:
        print("Please type a number")
        guess = int(input("Pick a number between 1 and 10  "))
    while guess != answer:
        tries += 1
        if guess > answer:
            try:
                guess = int(input("try again but guess lower  "))
            except ValueError:
                print("Please type a number")
                guess = int(input("try again but guess lower  "))
        if guess < answer:
            try:
                guess = int(input("try agian but guess higher  "))
            except ValueError:
                print("Please type a number")
                guess = int(input("try again but guess higher "))
        if guess == answer:
            tries += 1
            print("Hey nice work that was the correct number")
            print("and it only took you {} tires".format(tries))



start_game()
