# Problem given by Harry from Code with Harry Youtube Channel (HarisAK)
# Coder - Praveen Singh Chauhan (Technology Video Network - Youtube Channel , GAMP Aaryawarti Films - Film Production & Youtube Channel)
# Link of Youtube - https://www.youtube.com/TechnologyVideoNetwork , https://www.youtube.com/gampaaryawartifilms
# Facebook - https://www.facebook.com/praveen13c
# Twitter - https://twitter.com/praveen13c , https://twitter.com/tvnutube
# Linkedin -  https://www.linkedin.com/in/impraveenchauhan


the_number = 13
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
            print(f"Your Mobile Number is {mob_num}")
            print("HINT = number has two digit and bigger than 10 smaller to 25 ")
        elif len(mob_num) < 10 and guess_count == 3:

            if len(mob_num) < 10 and len(mob_num) > 3 and guess_count == 3:
                print(f"You Missed the Chance to get a hint")
                print("Message : You entered a too big number...\n")
                guess_count += 1
            else:
                print("*" * 70)
                print(f"You Missed the Chance to get a hint, \n"
                f"Its not a 10 digit mobile number {guess_number} . its only {len(mob_num)} digit long ")
                guess_count += 1
        else:

            if len(mob_num) <= 10 and  len(mob_num) >= 3:
                guess_count += 1
                print("*" * 25)
                print("Message  = Number you entered is too big.. \n")
            else:
                guess_count += 1
                print(f"Your given number {guess_number} is 'Bigger'....\n")
    elif guess_number == the_number:
        print(f"Congratulations .... you guessed right, '[ {guess_number} ]' ")
        break
    else:
        print("errrrrooorrr ")
# End of the Program
