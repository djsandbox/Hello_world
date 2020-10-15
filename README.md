# Setup, we call these later
yes_no = ["yes", "no"]
directions = ["left", "right", "forward", "backward"]
wizard = ["Shoot him, Chant back, run"]
chest = ["Open it, Run past"]
light = ["Walk to it, Turn around"]
 
# Introduction
name = input("What is your name?")
# this is where they ask you what your name is 
print("This is case sensitive, meaning you need to use capitals or else it wont work.")
print("Greetings, " + name + ". Lets have an adventure!")
print("You find yourself on the edge of a dark forest.")
print("Can you find your way through?")
 
# Start of game 
response = ""
while response not in yes_no:
    response = input("Would you like to step into the forest?\nyes/no\n")
    if response == "yes":
        print("You head into the forest. You hear crows cawwing in the distance.\n")
    elif response == "no":
        print("You are not ready for this quest. Goodbye, " + name + ".")
        quit()
    else: 
        print("I didn't understand that.\n")
 
# Next part of game
response = ""
while response not in directions:
    print("To your left, you see a bear.")
    print("To your right, there is more forest.")
    print("There is a rock wall directly in front of you.")
    print("Behind you is the forest exit.\n")
    response = input("What direction do you move?\nleft/right/forward/backward\n")
# this is where is asks you which direction and you would choose which way you would like to go 
    if response == "left":
        print("The bear eats you. Farewell, " + name + ".")
        quit()
    elif response == "right":
        print("You head deeper into the forest. As you walk, you come across a wizard chanting some weird ass words.\n")
        print("What do you do?\n")
        repsonse = ""
        while response not in wizard:
          print("Shoot him with your backup gun")
          print("Chant random words back")
          print("Run away")
          response = input("Shoot him/Chant back/Run")
          if response == "Shoot him":
            print("You learned the hard way that wizards are not only bulletproof, but reflect any and all bullets. You are dead.")
            quit()
          elif response == "Chant back":
            print("By spouting random words, you manage to harness your inner chi and cast a fireball big enough to annihilate an entire planet, ending your quest. You win, I guess?")
            quit()
          elif response == "Run":
            print("As you run, you start to realize that this forest was a waste of time to explore. You find the exit and leave, thankful to be alive. You didn't finish the adventure, but you still have your life, so you win.")
            quit()
    elif response == "forward":
        print("You climb the wall, to find a treasure chest ontop of it. What do you do?\n")
        response = ""
        while response not in chest:
          print("Open the chest")
          print("Run past it")
          response = input("Open it/Run past")
          if response == "Open it":
            print("You walk up to the chest, too blinded by greed to notice that there is a giant lava pool surrounding the chest. You fall into the lava. You are dead")
            quit()
          elif response == "Run past":
            print("You decide that the chest isn't worth it, and as you walk by, you notice the giant lava pit surrounding the chest. Good thing you didn't go to open it! ...Right?\n")
            print("As you continue to walk in the forest, you start to see a bright light. What do you do?\n")
            response = ""
            while response not in light:
              print("Walk towards the light")
              print("Turn around")
              response = input("Walk to it/Turn around")
              if response == "Walk to it":
                print("It turns out that the light source was the exit of the forest. You exit the forest and head back home. You win!")
                quit()
              elif response == "Turn around":
                print("You turn around and decide to stay in the forest forever. You build a house, forage for food, and slowly lose your mind as you never see the light of day again. I guess you lose?")
                quit()
        response = "" 
    elif response == "backward":
        print("You leave the forest. Goodbye, " + name + ".")
        quit()
    else:
        print("I didn't understand that.\n")
