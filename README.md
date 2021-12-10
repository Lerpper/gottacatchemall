# gottacatchemall
this program runs a simulation of pokemon


import random

def check(a,b):
    while 1 == 1:
        user = int(input("\n enter your choice: "))
        if user < a or user > b:
            print("\n please enter a valid input")
        else:
            return user
            break

def convert(pick2):
    #this function converts from their string to numerical value and vice versa
    #very helpful for a lot of things
    if pick2 == "Blastoise":
        return 0
    elif  pick2 == "Venusaur":
        return 1
    elif  pick2 == "Charizard":
        return 2
    elif  pick2 == "Raichu":
        return 3
    elif  pick2 == "Gyarados":
        return 4
    elif  pick2 == "Alakazam":
        return 5
    elif  pick2 == 0:
        return "Blastoise"
    elif  pick2 == 1:
        return "Venusaur"
    elif  pick2 == 2:
        return "Charizard"
    elif  pick2 == 3:
        return "Raichu"
    elif pick2 == 4:
        return "Gyarados"
    elif pick2 == 5:
        return "Alakazam"
def assignhp(a):
    #this function assigns hp, makes it easier to make adjustments all in one place
    Blastoisehp = 139
    Venusaurhp = 140
    Charizardhp = 138
    Raichuhp = 120
    Gyaradoshp = 155
    Alakazamhp = 115
    a = convert(a)
    if convert(a) == 0:
        return Blastoisehp
    elif convert(a) == 1:
        return Venusaurhp
    elif convert(a) == 2:
        return Charizardhp
    elif convert(a) == 3:
        return  Raichuhp
    elif convert(a) == 4:
        return  Gyaradoshp
    elif convert(a) == 5:
        return  Alakazamhp

def assignsp(a):
    #this function assigns speed, makes it easier to make adjustments all in one place
    Blastoisesp = 78
    Venusaursp = 80
    Charizardsp = 100
    Raichusp = 110
    Gyaradossp = 81
    Alakazamsp = 120
    a = convert(a)
    if convert(a) == 0:
        return Blastoisesp
    elif convert(a) == 1:
        return Venusaursp
    elif convert(a) == 2:
        return Charizardsp
    elif convert(a) == 3:
        return  Raichusp
    elif convert(a) == 4:
        return  Gyaradossp
    elif convert(a) == 5:
        return  Alakazamsp

def moninfo(a,b):
    #a is the mon
    #b is the info needed (1-4) are moves 5 is mon type
    a = convert(a)
    if convert(a) == 0:
        if b == 1:
            return "surf"
        if b == 2:
            return "flash cannon"
        if b == 3:
            return "bite"
        if b == 4:
            return "earthquake"
        if b == 5:
            return "water"
    elif convert(a) == 1:
        if b == 1:
            return "seed bomb"
        if b == 2:
            return "earthquake"
        if b == 3:
            return "venoshock"
        if b == 4:
            return "body slam"
        if b == 5:
            return "grass poison"
    elif convert(a) == 2:
        if b == 1:
            return "flamethrower"
        if b == 2:
            return "dragon breath"
        if b == 3:
            return "air slash"
        if b == 4:
            return "steel wing"
        if b == 5:
            return "fire flying"
    elif convert(a) == 3:
        if b == 1:
            return "thunderbolt"
        if b == 2:
            return "body slam"
        if b == 3:
            return "surf"
        if b == 4:
            return "play rough"
        if b == 5:
            return "electric"
    elif convert(a) == 4:
        if b == 1:
            return "surf"
        if b == 2:
            return "ice fang"
        if b == 3:
            return "crunch"
        if b == 4:
            return "dragon pulse"
        if b == 5:
            return "water flying"
    elif convert(a) == 5:
        if b == 1:
            return "psycic"
        if b == 2:
            return "shadow ball"
        if b == 3:
            return "ice punch"
        if b == 4:
            return "dazzling gleam"
        if b == 5:
            return "psycic"

def monmove(a,b,c):
    #a is the mon
    #b is the move number
    #c, 1 is for the damage, 2 is for the move type
    a = convert(a)
    if convert(a) == 0:
        if b == 1:
            # "surf"
            if c == 1:
                return 90
            if c == 2:
                return "water"
        if b == 2:
            # "flash cannon"
            if c == 1:
                return 80
            if c == 2:
                return "steel"
        if b == 3:
            # "bite"
            if c == 1:
                return 60
            if c == 2:
                return "dark"
        if b == 4:
            # "earthquake"
            if c == 1:
                return 100
            if c == 2:
                return "ground"
    if convert(a) == 1:
        if b == 1:
            if c == 1:
                return 80
            if c == 2:
                return "grass"
        if b == 2:
            if c == 1:
                return 100
            if c == 2:
                return "ground"
        if b == 3:
            if c == 1:
                return 65
            if c == 2:
                return "poison"
        if b == 4:
            if c == 1:
                return 85
            if c == 2:
                return "normal"
    if convert(a) == 2:
        if b == 1:
            if c == 1:
                return 90
            if c == 2:
                return "fire"
        if b == 2:
            if c == 1:
                return 60
            if c == 2:
                return "dragon"
        if b == 3:
            if c == 1:
                return 75
            if c == 2:
                return "flying"
        if b == 4:
            if c == 1:
                return 70
            if c == 2:
                return "steel"
    if convert(a) == 3:
        if b == 1:
            if c == 1:
                return 90
            if c == 2:
                return "electric"
        if b == 2:
            if c == 1:
                return 85
            if c == 2:
                return "normal"
        if b == 3:
            if c == 1:
                return 90
            if c == 2:
                return "water"
        if b == 4:
            if c == 1:
                return 90
            if c == 2:
                return "fairy"
    if convert(a) == 4:
        if b == 1:
            # "surf"
            if c == 1:
                return 90
            if c == 2:
                return "water"
        if b == 2:
            if c == 1:
                return 65
            if c == 2:
                return "ice"
        if b == 3:
            if c == 1:
                return 80
            if c == 2:
                return "dark"
        if b == 4:
            if c == 1:
                return 85
            if c == 2:
                return "dragon"
    if convert(a) == 5:
        if b == 1:
            if c == 1:
                return 90
            if c == 2:
                return "psycic"
        if b == 2:
            if c == 1:
                return 80
            if c == 2:
                return "ghost"
        if b == 3:
            if c == 1:
                return 75
            if c == 2:
                return "ice"
        if b == 4:
            if c == 1:
                return 80
            if c == 2:
                return "fairy"



def typeweakness(a,b):
    eff = 1
#a is defending type
#b is attacking type
    if "normal" in a:
        if "fighting" in b:
            eff *= 2
        if "ghost" in b:
            eff = 0
    if "fire" in a:
        if "fire" in b:
            eff /= 2
        if "water" in b:
            eff *= 2
        if "grass" in b:
            eff /= 2
        if "ice" in b:
            eff /= 2
        if "ground" in b:
            eff *= 2
        if "bug" in b:
            eff /= 2
        if "rock" in b:
            eff *= 2
        if "fairy" in b:
            eff /= 2
        if "steel" in b:
            eff /= 2
    if "water" in a:
        if "fire" in b:
            eff /= 2
        if "water" in b:
            eff /= 2
        if "grass" in b:
            eff *= 2
        if "electric" in b:
            eff *= 2
        if "ice" in b:
            eff /= 2
        if "steel" in b:
            eff /= 2
    if "grass" in a:
        if "fire" in b:
            eff *= 2
        if "water" in b:
            eff /= 2
        if "grass" in b:
            eff /= 2
        if "electric" in b:
            eff /= 2
        if "ice" in b:
            eff *= 2
        if "poison" in b:
            eff *= 2
        if "ground" in b:
            eff /= 2
        if "fighting" in b:
            eff *= 2
        if "bug" in b:
            eff *= 2
    if "electric" in a:
        if "electric" in b:
            eff /= 2
        if "ground" in b:
            eff *= 2
        if "flying" in b:
            eff /= 2
        if "steel" in b:
            eff /= 2
    if "ice" in a:
        if "bug" in b:
            eff *= 2
    if "fighting" in a:
        if "bug" in b:
            eff *= 2
    if "poison" in a:
        if "bug" in b:
            eff *= 2
    if "ground" in a:
        if "bug" in b:
            eff *= 2
    if "flying" in a:
        if "grass" in b:
            eff /= 2
        if "electric" in b:
            eff *= 2
        if "ice" in b:
            eff *= 2
        if "fighting" in b:
            eff /= 2
        if "ground" in b:
            eff = 0
        if "rock" in b:
            eff *= 2
        if "bug" in b:
            eff /= 2
    if "psycic" in a:
        if "Fighting" in b:
            eff /= 2
        if "psycic" in b:
            eff /= 2
        if "bug" in b:
            eff *= 2
        if "ghost" in b:
            eff *= 2
        if "dark" in b:
            eff *= 2
    if "bug" in a:
        if "bug" in b:
            eff *= 2
    if "rock" in a:
        if "bug" in b:
            eff *= 2
    if "ghost" in a:
        if "bug" in b:
            eff *= 2
    if "dragon" in a:
        if "bug" in b:
            eff *= 2
    if "dark" in a:
        if "bug" in b:
            eff *= 2
    if "steel" in a:
        if "bug" in b:
            eff *= 2
    if "fairy" in a:
        if "bug" in b:
            eff *= 2
    return eff

def attack(a,b,c):
    #a is the attacking mon
    #b is the move number
    #c is the defending pokemon
            print("{} uses {}".format(convert(a),moninfo(a,b)))
            incomingdamage = monmove(a,b,1)
            incomingtype = monmove(a,b,2)
            defendingtype = moninfo(c,5)
            eff = typeweakness(defendingtype,incomingtype)
            damage = incomingdamage * eff
            return damage

def game_end(a):
    if a == 1:
        print("all of your mons fainted, you lose")
        while 1 == 1:
            pause = input()
    if a == 2:
        print("all oposing mons fainted, you win")
        while 1 == 1:
            pause = input()

    

def gamestate(mon1,mon2,mon3,mon4,mon5,mon6):
    mons = ["Blastoise","Venusaur","Charizard","Raichu","Gyarados","Alakazam"]
    print("\n Who would you like to send out first? \n 1. {} \n 2. {} \n 3. {}".format(mons[mon1],mons[mon2],mons[mon3]))
    first = check(1,3)
    if first == 1:
        currentmon = mon1
    elif first== 2:
        currentmon = mon2
    elif first ==3:
        currentmon = mon3
    cpu = random.randint(1,3)
    if cpu == 1:
        opcurrentmon = mon4
    elif cpu == 2:
        opcurrentmon = mon5
    elif cpu ==3:
        opcurrentmon = mon6
    #
    mon1hp = assignhp(mon1)
    mon2hp = assignhp(mon2)
    mon3hp = assignhp(mon3)
    mon4hp = assignhp(mon4)
    mon5hp = assignhp(mon5)
    mon6hp = assignhp(mon6)
    mon1sp = assignsp(mon1)
    mon2sp = assignsp(mon2)
    mon3sp = assignsp(mon3)
    mon4sp = assignsp(mon4)
    mon5sp = assignsp(mon5)
    mon6sp = assignsp(mon6)



    while 1==1:
        if currentmon == mon1:
            currentmonhp = mon1hp
            currentmonsp = mon1sp
        elif currentmon == mon2:
            currentmonhp = mon2hp
            currentmonsp = mon2sp
        elif currentmon == mon3:
            currentmonhp = mon3hp
            currentmonsp = mon2sp

        if opcurrentmon == mon4:
            opcurrentmonhp = mon4hp
            opcurrentmonsp = mon4sp
        elif opcurrentmon == mon5:
            opcurrentmonhp = mon5hp
            opcurrentmonsp = mon5sp
        elif opcurrentmon == mon6:
            opcurrentmonhp = mon6hp
            opcurrentmonsp = mon6sp
        faint = False
        myfaint = False

        back = False
        print("--------------------------------------------------------------")
        print("|                                                            |")
        print("|    {}                                                  |".format(convert(opcurrentmon)))
        print("|                      HP: {}                                |".format(opcurrentmonhp))
        print("|                                                            |")
        print("|                                                            |")
        print("|                                                            |")
        print("|                                                            |")
        print("|                                                            |")
        print("|                                                            |")
        print("|                                                            |")
        print("|                                                            |")
        print("|                                                            |")
        print("|                                                            |")
        print("|                                                            |")
        print("|                                                            |")
        print("|                                                            |")
        print("|    {}                                                  |".format(convert(currentmon)))
        print("|                      HP: {}                                |".format(currentmonhp))
        print("|                                                            |")
        print("--------------------------------------------------------------\n")
        print("1. fight                    2.pokemon")



        user_choice = check(1,4)
        if user_choice == 1:
            print(" 1. {} \n 2. {} \n 3. {} \n 4. {} \n".format(moninfo(currentmon,1),moninfo(currentmon,2),moninfo(currentmon,3),moninfo(currentmon,4)))
            move_choice = check(1,4)

            if currentmonsp > opcurrentmonsp:
                opcurrentmonhp-=attack(currentmon,move_choice,opcurrentmon)
                if opcurrentmonhp <= 0:
                    faint = True
                    print("{} fainted\n".format(convert(opcurrentmon)))

                    if opcurrentmon == mon4:
                        mon4hp = opcurrentmonhp
                    elif opcurrentmon == mon5:
                        mon5hp = opcurrentmonhp
                    elif opcurrentmon == mon6:
                        mon6hp = opcurrentmonhp

                    if mon4hp > 0:
                        opcurrentmon = mon4
                    elif mon5hp > 0:
                        opcurrentmon = mon5
                    elif mon6hp > 0:
                        opcurrentmon = mon6
                    else:
                        game_end(2)
                    print("computer sent in {}\n".format(convert(opcurrentmon)))
                else:
                    cpu_move = random.randint(1,4)
                    currentmonhp-=attack(opcurrentmon,cpu_move,currentmon)
                    if currentmonhp <= 0:
                        myfaint = True
                        print("{} fainted\n".format(currentmon))

                        if currentmon == mon1:
                            mon1hp = currentmonhp
                        elif currentmon == mon2:
                            mon2hp = currentmonhp
                        elif currentmon == mon3:
                            mon3hp = currentmonhp

                        
                        if mon1hp < 1 and mon2hp < 1 and mon3hp < 1:
                            game_end(1)
                        print("Which mon would you like to send out?")
                        if mon1hp > 0:
                            print("1. {}".format(convert(mon1)))
                        if mon2hp > 0:
                            print("2. {}".format(convert(mon2)))
                        if mon3hp > 0:
                            print("3. {}".format(convert(mon3)))
                        put = check(1,3)
                        if put == 1:
                            currentmon = mon1
                        elif put == 2:
                            currentmon = mon2
                        elif put == 3:
                            currentmon = mon3
                        print("you sent out {}\n".format(convert(currentmon)))
            else:
                cpu_move = random.randint(1,4)
                currentmonhp-=attack(opcurrentmon,cpu_move,currentmon)
                if currentmonhp <= 0:
                    myfaint = True
                    print("{} fainted\n".format(convert(currentmon)))

                    if currentmon == mon1:
                        mon1hp = currentmonhp
                    elif currentmon == mon2:
                        mon2hp = currentmonhp
                    elif currentmon == mon3:
                        mon3hp = currentmonhp
                    if mon1hp < 1 and mon2hp < 1 and mon3hp < 1:
                            game_end(1)
                    print("Which mon would you like to send out?")
                    if mon1hp > 0:
                        print("1. {}".format(convert(mon1)))
                    if mon2hp > 0:
                        print("2. {}".format(convert(mon2)))
                    if mon3hp > 0:
                        print("3. {}".format(convert(mon3)))
                    put = check(1,3)
                    if put == 1:
                        currentmon = mon1
                    elif put == 2:
                        currentmon = mon2
                    elif put == 3:
                        currentmon = mon3
                    print("you sent out {}\n".format(convert(currentmon)))
                else:
                    opcurrentmonhp-=attack(currentmon,move_choice,opcurrentmon)
                    if opcurrentmonhp <= 0:
                        faint = True
                        print("{} fainted\n".format(convert(opcurrentmon)))

                        if opcurrentmon == mon4:
                            mon4hp = opcurrentmonhp
                        elif opcurrentmon == mon5:
                            mon5hp = opcurrentmonhp
                        elif opcurrentmon == mon6:
                            mon6hp = opcurrentmonhp

                        if mon4hp > 0:
                            opcurrentmon = mon4
                        elif mon5hp > 0:
                            opcurrentmon = mon5
                        elif mon6hp > 0:
                            opcurrentmon = mon6
                        else:
                            game_end(2)
                        print("computer sent in {}\n".format(convert(opcurrentmon)))

        elif user_choice == 2:
            while 1==1:
                print("to swap use the command \"swap #\" where # is the mon you want to swap in")
                print("For more info on a mon use the command \" info #\" where # is the mon you want more info on")
                print("to go back type \"back\"")
                print("\n 1. {} \n 2. {} \n 3. {} \n".format(mons[mon1],mons[mon2],mons[mon3]))
                monscreen = input()
                if "swap" in monscreen.lower():
                    if "1" in monscreen:
                        if mon1 == currentmon:
                            print("this mon is already in")
                        elif mon2hp < 1:
                            print("this mon has feinted")
                        else:
                            currentmon = mon1
                            print("you swapped in {}".format(convert(mon1)))
                            break
                    elif "2" in monscreen:
                        if mon2 == currentmon:
                            print("this mon is already in")
                        elif mon2hp < 1:
                            print("this mon has feinted")
                        else:
                            currentmon = mon2
                            print("you swapped in {}".format(convert(mon2)))
                            break
                    elif "3" in monscreen:
                        if mon3 == currentmon:
                            print("this mon is already in")
                        elif mon3hp < 1:
                            print("this mon has feinted")
                        else:
                            currentmon = mon3
                            print("you swapped in {}".format(convert(mon3)))
                            break
                    else:
                        print("please enter a valid option")
                elif "info" in monscreen.lower():
                    if "1" in monscreen:
                        print("Name: {} type: {}".format(convert(mon1),moninfo(mon1,5)))
                        print(" 1. {} \n 2. {} \n 3. {} \n 4. {} \n".format(moninfo(mon1,1),moninfo(mon1,2),moninfo(mon1,3),moninfo(mon1,4)))
                        pause = input("press enter to continue")
                    elif "2" in monscreen:
                        print("Name: {} type: {}".format(convert(mon2),moninfo(mon2,5)))
                        print(" 1. {} \n 2. {} \n 3. {} \n 4. {} \n".format(moninfo(mon2,1),moninfo(mon2,2),moninfo(mon2,3),moninfo(mon2,4)))
                        pause = input("press enter to continue")
                    elif "3" in monscreen:
                        print("Name: {} type: {}".format(convert(mon3),moninfo(mon3,5)))
                        print(" 1. {} \n 2. {} \n 3. {} \n 4. {} \n".format(moninfo(mon3,1),moninfo(mon3,2),moninfo(mon3,3),moninfo(mon3,4)))
                        pause = input("press enter to continue")
                    else:
                        print("please enter a valid option")
                elif "back" in monscreen.lower():
                    back = True
                    break
                else:
                    print("please enter a valid option")
            if back == False:
                cpu_move = random.randint(1,4)
                currentmonhp-=attack(opcurrentmon,cpu_move,currentmon)
                if currentmonhp <= 0:
                    myfaint = True
                    print("{} fainted".format(currentmon))

                    if currentmon == mon1:
                        mon1hp = currentmonhp
                    elif currentmon == mon2:
                        mon2hp = currentmonhp
                    elif currentmon == mon3:
                        mon3hp = currentmonhp

                    print("Which mon would you like to send out?")
                    if mon1hp > 0:
                        print("1. {}".format(mon1))
                    if mon2hp > 0:
                        print("2. {}".format(mon2))
                    if mon3hp > 0:
                        print("3. {}".format(mon3))
                    put = check(1,3)
                    if put == 1:
                        currentmon = mon1
                    elif put == 2:
                        currentmon = mon2
                    elif put == 3:
                        currentmon = mon3
                    print("you sent out {}".format(currentmon))

        if myfaint == False:
            if currentmon == mon1:
                mon1hp = currentmonhp
            elif currentmon == mon2:
                mon2hp = currentmonhp
            elif currentmon == mon3:
                mon3hp = currentmonhp

        if faint == False:
            if opcurrentmon == mon4:
                mon4hp = opcurrentmonhp
            elif opcurrentmon == mon5:
                mon5hp = opcurrentmonhp
            elif opcurrentmon == mon6:
                mon6hp = opcurrentmonhp

def main():
    mons = ["Blastoise","Venusaur","Charizard","Raichu","Gyarados","Alakazam"]
    draft = ["Blastoise","Venusaur","Charizard","Raichu","Gyarados","Alakazam"]
    print()
    count = 1
    for x in draft:
        print("{}. {}".format(count,x))
        count+=1
    pick = check(1,len(draft))
    pick-=1
    draft.pop(pick)
    cpu_pick = random.randint(1,len(draft))
    print("\n The computer picked {} \n".format(draft[cpu_pick - 1]))
    cpick = draft.pop(cpu_pick - 1)
    cpick = convert(cpick)
    count = 1
    for x in draft:
        print("{}. {}".format(count,x))
        count+=1
    pick1 = check(1,len(draft))
    pick1-=1
    pick1 = draft.pop(pick1)
    pick1 = convert(pick1)
    cpu_pick1 = random.randint(1,len(draft))
    print("\n The computer picked {} \n".format(draft[cpu_pick1 - 1]))
    cpick1 = draft.pop(cpu_pick1 - 1)
    cpick1 = convert(cpick1)
    count = 1
    for x in draft:
        print("{}. {}".format(count,x))
        count+=1
    pick2 = check(1,len(draft))
    pick2-=1
    pick2 = draft.pop(pick2)
    pick2 = convert(pick2)
    print("\n The computer got {}".format(draft[0]))
    cpick2 = convert(draft[0])
    


    print("\n your pokemon are {}, {}, and {}".format(mons[pick],mons[pick1],mons[pick2]))

    gamestate(pick,pick1,pick2,cpick,cpick1,cpick2)
    
main()
