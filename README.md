# Exercise to make a guess game given by Harry from Code with Harry youtube channel
# Coder - Praveen Singh Chauhan

the_number = 18
guess_number = 0
guess_count = 0
left_chance = 0
total_chance = 9

while True:

    if guess_count == 9:
        print("*" * 45)
        print("SO Sorry.. Your have exhaust all your chances ")
        print("*" * 45)
        break
    elif guess_count == 3:
        print("if you want a hint type your mobile number , but u've to sacrifice 2 attempts")

    left_chance = total_chance - guess_count
    print("<>", "=" * 30, "<>")
    print("  GUESS THE RIGHT NUMBER - G A M E ")
    print(f"    You have ( {left_chance} ) chances left ")
    print("<>", "=" * 30, "<>")
    guess_number = int(input("Enter Your Number > "))
    mob_num = str(guess_number)

    if guess_number < the_number:
        guess_count += 1
        print(f"Your given number {guess_number} is 'Smaller'...\n")
    elif guess_number > the_number:
        mob_num = str(guess_number)
        if len(mob_num) == 10 and guess_count == 3:
            guess_count += 2
            print("*" * 25)
            print("HINT = number has two digit and smaller to 25 ")
        elif len(mob_num) < 10 and guess_count == 3:
            print("*" * 70)
            print(f"You Missed the Chance to get a hint, \n"
                  f"Its not a 10 digit mmobile number {guess_number} . its only {len(mob_num)} digit long ")
            guess_count += 1
        else:
            guess_count += 1
            print(f"Your given number {guess_number} is 'Bigger'....\n")
    elif guess_number == the_number:
        print(f"Congratulations .... you guessed right, '[ {guess_number} ]' ")
        break
    else:
        print("errrrrooorrr ")
# End of the Program
