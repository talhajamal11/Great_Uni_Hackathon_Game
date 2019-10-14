#definitions
import time
from random import randint
inventory = [None]
power = False
fuel = False
cmdlist = None
recipe = {'Memes':'6363'}
alien = {'elec' : True, 'vent' :True}
#introduction
print("\n Welcome to Them!")
print("This is a text-based adventure game.")
print("To play the game, type your response to each prompt.")
print("Typing 'INVENTORY' tells you what you're carrying.")
print("Type 'HELP' at any time for game instructions.")
print("Type 'CRAFT' to view recipe & craft items.")
print("Type 'QUIT' to quit the game.")
#start of game
def start():
    print("\n Walking out of the airlock")
    print('Where do you go?')
    print('1 - Corridor 1')
    print('2 - Back to Expedition Ship')

    cmdlist = ['1', '2']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        cor1()
    elif cmd == '2':
        expe()

#corridor1
def cor1():
    time.sleep(0.5)
    print("\n CORRIDOR 1")
    print("There are 8 rooms")
    print("1 - Airlock leading to the Expedition Shuttle")
    print("2 - Spacesuit closet")
    print("3 - Maintainance room")
    print("4 - A locked room that only the captain has access to")
    print("5 - Central Air Ventilation System")
    print("6 - Bio-Chemistry Laboratory")
    print("7 - Medical Bay")
    print("8 - The Central Hub")

    cmdlist = ['1', '2', '3', '4','5','6','7','8']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        expe()
    elif cmd == '2':
        closet()
    elif cmd == '3':
        supply()
    elif cmd == '4':
        if 'cap_card' in inventory:
            SECRET()
        else:
            print('\nCaptain''s Storage - LOCKED, ACCESS DENIED')
            cor1()
    elif cmd == '5':
        cen_AC()
    elif cmd == '6':
        lab_biochem()
    elif cmd == '7':
        med_bay()
    elif cmd == '8':
        hub()
def expe():
    print("\nYou strap in, ready to get off this ship")
    time.sleep(1)
    print("\nUNDOCKING")
    time.sleep(3)
    print("\nThe shuttle detaches")
    time.sleep(2)
    if fuel == True:
        print("\nMicro thrusters clear the shuttle from the vicinity of the ship")
        victory()
    else:
        print("\nThere's not enough fuel")
        time.sleep(2)
        print("\nEngine shuts down")
        time.sleep(1)
        print("\nYou are trapped")
        dead()
def cen_AC():
    time.sleep(0.5)
    print("\n Central Air Ventilation Control Room")
    print("There is a vent big enough to crawl through here.")
    if 'torch' in inventory or power == True:
        print("You can make your way up to the upper deck, where the control room is,")
        print("or down to the storage area.")
        print("1 - Upper Deck")
        print("2 - Storage Area")
    else:
        print("It's pitch black inside the vent, you are not sure where they lead")
        print("1 - ?????")
        print("2 - ?????")
    print("3 - Corridor 1")
    cmdlist = ['1', '2','3','4']
    cmd = getcmd(cmdlist)
    if cmd == '1':
        print("\nThe vent is pitch black")
        time.sleep(2)
        print("Clanking can be heard up ahead")
        print("Investigate ?")
        print("1 - Yes")
        print("2- No")
        cmdlist = ['1','2']
        cmd = getcmd(cmdlist)
        if cmd == '1':
            print("\nThis should lead to the control room")
            print("You keep crawling")
            time.sleep(2)
            print("*clanking stops*")
            print("*silence*")
            time.sleep(3)
            dead()
        elif cmd == '2':
            print("\nYou are back in the")
            cen_AC()
    elif cmd == '2':
        print("\nYou arrive at the storage unit")
        storage()
    elif cmd =='3':
        print("\nYou are back in")
        cor1()
def closet():
    print("\n Closet")
    print("There are spacesuits for expeditions like the one you have on. You don't need them on the ship.")
    print("1 - Corridor 1")#needs fixing - add bag?
    cmdlist = ['1']
    cmd = getcmd(cmdlist)
    if cmd == '1':
        cor1()
def supply():
    print("\nMaintainance room")
    print("There are tools for carrying out minor repairs.")
    if 'torch' not in inventory:
        print("A torch lies on the floor")
    print("1 - Corridor 1")
    if 'torch' not in inventory:
        print("2 - Pick up torch")
    cmdlist = ['1','2']
    cmd = getcmd(cmdlist)
    if cmd == '1':
        cor1()
    elif cmd == '2':
        additem('torch')
        supply()
def SECRET():
    print("\n There's a massive f**king hole in the hull of the ship")
    print("---!!!---")
    print("The pressure differential sucks you out into space")
    print("You ded")
    print("RIP Squidward")
    nothing = input()
    exit()
def med_bay():
    time.sleep(0.5)
    print("\n Medical Bay")
    print("It has been trashed but most of the items you’d expect to find are still there.")
    print("Several first aid kits lie on the desk.")
    if 'scalpel' not in inventory:
        print("A scalpel lies on the floor.")
        print("Not very hygienic but it could come in handy later on….")
    print("1 - Corridor 1")
    if 'scalpel' not in inventory:
        print("2 - Pick up scalpel")
    cmdlist = ['1','2']
    cmd = getcmd(cmdlist)
    if cmd == '1':
        cor1()
    elif cmd == '2':
        additem("scalpel")
        med_bay()
#MAIN HUB
def hub():
    time.sleep(0.5)
    print("\n HUB")
    print("The central part of the main floor of the ship.")
    if 'metalpipe' not in inventory:
        print("Pieces of metal piping litter one side of the room.")
    print("Damage seems to have been done to the wall and ceiling.")
    print("The furniture is ripped and the wall monitor is smashed on the floor.")
    print("1 - Corridor 1")
    print("2 - Corridor 2")
    print("3 - Corridor 3")
    print("4 - Corridor 4")
    print("5 - Corridor 5")
    if 'metalpipe' not in inventory:
        print("6 - Pick up one of the pipes")

    cmdlist = ['1', '2', '3', '4','5','6']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        cor1()
    elif cmd == '2':
        cor2()
    elif cmd == '3':
        cor3()
    elif cmd == '4':
        cor4()
    elif cmd == '5':
        cor5()
    elif cmd == '6':
        additem('metalpipe')
        hub()
def recreational_gym():
    print("\n The gym")
    #needs fixing
    hub()
def cry():
    print("\nOne of the cryogenic chambers where the crew is kept in stasis while the ship travels for centuries further into space.")
    hub()

def lab_biochem():
    time.sleep(0.5)
    print("\n BioChemical Lab")
    print("\nDo you smell it?")
    print("The smell? A kind of smelly smell, a smelly smell that smells ... smelly.")
    print("Or maybe that’s just the smell of the fertiliser.")
    print("Microscopes and test tubes lie scattered across the tables.")
    if 'torch' in inventory or power == True:
        if 'mold' not in inventory:
            print("On the desk, a container of a mold sample collected on the ship.")
            print("It excreets acid capable of degrading metal.")
    print("1 - Collect fertiliser")
    print("2 - Smell fertiliser")
    print("3 - Corridor 1")
    if 'torch' in inventory or power == True:
        if 'mold' not in inventory:
            print("4 - Collect mold")
    cmdlist = ['1', '2', '3','4']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        additem("fertiliser")
        lab_biochem()
    elif cmd == '2':
        print("\nIt smells smelly")
        lab_biochem()
    elif cmd == '3':
        cor1()
    elif cmd == '4':
        additem("mold")
        lab_biochem()

#corridor2
def cor2():
    time.sleep(0.5)
    print("\n CORRIDOR 2")
    print("There are 5 rooms")
    print("1 - Study Room")
    print("2 - Cryogenic Chamber 2")
    print("3 - Cryogenic Chamber 3")
    print("4 - Lift")
    print("5 - Materials Lab")
    print("6 - Hub")

    cmdlist = ['1', '2', '3', '4','5','6']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        study_room()
    elif cmd == '2':
        cry()
    elif cmd == '3':
        cry()
    elif cmd == '4':
        if power == True:
            lift()
        else:
            print("The power is OFF. The emergency power is not enough to operate the lift")
            cor2()
    elif cmd == '5':
        lab_mat()
    elif cmd == '6':
        hub()
def lab_mat():
    print("Materials laboratory")

def study_room():
    time.sleep(0.5)
    print("\n There are plenty of physical and digital books in here.")
    print("The study lounge is divided into sections:\n -Biology\n -Chemistry\n -General\n -Physics\n -...\n")
    print("Your crewmate Kirthana is hunched over a desk, lifeless and bloody.")
    print("1 - Corridor 2")
    print("2 - Examine Kirthana's body")
    cmdlist = ['1', '2']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        cor2()
    elif cmd == '2':
        print("On her holographic bracelet, a book titled 'Boom!: The Chemistry and History of Explosives' is still opened.")
        print("Must be the last thing she was doing before something got her.\n")
        time.sleep(1)
        print("Some texts were highlighted:")
        time.sleep(1.5)
        print("... In the early days of explosives, a mixture of ammonium nitrate and fuel oil called ANFO was widely used as a bulk indistrial explosive...")
        time.sleep(3.5)
        print("... ANFO is classified as a blasting agent, meaning that it decomposes through detonation...")
        time.sleep(3.5)
        print("... A larger quantity of secondary explosive, primer, must be used to set off ANFO, classifying it as a tertiary explosive...")
        time.sleep(3.5)
        recipe['Explosive']:'2006'
        study_room()
#corridor3
def cor3():
    time.sleep(0.5)
    print("\n CORRIDOR 3")
    print("There are 4 rooms")
    print("1 - Bedroom 2")
    print("2 - Bedroom 3")
    print("3 - Bedroom 4")
    print("4 - Hub")

    cmdlist = ['1', '2', '3', '4']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        bed2()
    elif cmd == '2':
        bed3()
    elif cmd == '3':
        bed4()
    elif cmd == '4':
        hub()
def bed2():
    print("\n There are two beds. One belonging to Emil and the other belonging to Louis.")
    print("On Louis' bed there is a note asking for help...")
    print("1 - Bathroom 2")
    print("2 - Corridor 3")#needs fixing - add mold notes
    cmdlist = ['1', '2']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        bath2()
    elif cmd == '2':
        cor3()
def bath2():
    print("\n You enter the bathroom. The stench is unbearable. You should probably leave.")
    print("1 - Bedroom 2")
    bed2()
def bed3():
    print("\n There are two beds. One belonging to Mitra and the other belonging to Kirthana.")
    print("There's a book titled 'Eragon' on one of the beds.")
    print("1 - Bathroom 3")
    print("2 - Corridor 3")
    cmdlist = ['1', '2']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        bath3()
    elif cmd == '2':
        cor4()
def bath3():
    time.sleep(0.5)
    print("\n You enter the bathroom. This one is actually pretty clean.")
    if 'spoiler#1' not in inventory:
        print("There's a scrunched up note in the toilet bowl")
        print("Someone was trying to flush it away")
    print("1 - Bedroom 3")
    if 'spoiler#1' not in inventory:
        print("2 - Pick up the note")
    cmdlist = ['1', '2']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        bed3()
    elif cmd == '2':
        print("\nThe note reads")
        time.sleep(3)
        print("Vision dies in Avengers Infinity War")
        additem('spoiler#1')
        bath3()
def bed4():
    time.sleep(0.5)
    print("\n Bedroom 4")
    print("This bedroom belongs to you and your companion.")
    print("It’s just as you left it.")
    if 'battery' not in inventory:
        print("The new lithium-ion battery you asked for to fix your lamp is on your bedside table.")
    print("1 - Bathroom 4")
    print("2 - Corridor 3")
    if 'battery' not in inventory:
        print("3 - Pick up battery")
    cmdlist = ['1', '2', '3']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        print("\nTheres nothing in the bathroom")
        bed4()
    if cmd == '2':
        cor3()
    elif cmd == '3':
        additem('battery')
        bed4()
def bath4():
    print("\n You enter the bathroom. The bin is full, it was your companion’s turn to empty it.")
    print("1 - Bedroom 4")
    bed4()

#corridor4
def cor4():
    time.sleep(0.5)
    print("\n CORRIDOR 4")
    print("There are 5 rooms")
    print("1 - Ladder going up")
    print("2 - Ladder going down")
    print("3 - Bedroom 1")
    print("4 - Captain's Room")
    print("5 - Hub")

    cmdlist = ['1', '2', '3', '4', '5']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        cor6()
    elif cmd == '2':
        ladder_bot()
    elif cmd == '3':
        bed1()
    elif cmd == '4':
        if 'cap_card' in inventory:
            cap_room()
        else:
            print("Captain's Room - ACCESS DENIED")
            cor4()
    elif cmd == '5':
        hub()
def bed1():
    print("\n This bedroom belongs to Minh and Marco. There is only a double bed")
    print("1 - Bathroom 1")
    print("2 - Corridor 4")
    cmdlist = ['1', '2']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        bath1()
    elif cmd == '2':
        cor4()
def bath1():
    print("\n You enter the bathroom. There are some bunny magazines besides the toilet.")
    print("1 - Bedroom 1")
    bed1()
def bedcap():
    print("\n This bedroom belongs to Cpt. Talha Jamal.")
    print("There is a suspicious amount of tissue beside the bed...")
    print("What’s left of Emil is on the floor grasping an orange he was no doubt hiding in TJ’s room as a part of his latest prank.")
    print("1 - Captain's Bathroom")
    print("2 - Corridor 4")
    cmdlist = ['1', '2']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        bathcap()
    elif cmd == '2':
        cor4()
def bathcap():
    print("\n This is the Captain's bathroom. The toilet is completely blocked.")
    print("An unreasonable amount of tissues and feces is splattered all over the toilet")
    print("1 - Captain's bedroom")
    cmdlist = ['1']
    cmd = getcmd(cmdlist)
    if cmd == '1':
        bedcap()
#corridor5
def cor5():
    time.sleep(0.5)
    print("\n CORRIDOR 5")
    print("There are 5 rooms")
    print("1 - Dining Room")
    print("2 - Kitchen")
    print("3 - Cryogenic Chamber 2")
    print("4 - Experimental Lab")
    print("5 - Hub")
    cmdlist = ['1', '2', '3', '4', '5']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        dine()
    elif cmd == '2':
        kitchen()
    elif cmd == '3':
        cry()
    elif cmd == '4':
        exlab()
    elif cmd == '5':
        hub()
def kitchen():
    time.sleep(0.5)
    print("\n You step over Minh's body as you enter the kitchen.")
    print("A clean container and some plates are next to the sink.")
    print("There is some chicken biryani on the counter.")
    print("It seems it was prepared not too long ago. But no one is to be seen.")
    print("1 - Dining room")
    print("2 - Corridor 5")
    print("3 - Pick up container")
    print("4 - Get some water")
    cmdlist = ['1', '2', '3','4']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        dine()
    elif cmd == '2':
        cor5()
    elif cmd == '3':
        additem('container')
        kitchen()
    elif cmd == '4':
        additem('water')
        kitchen()
def dine():
    print("\n You enter the dining room.")
    print("Broken plates and a pool of tea lie on the floor next to a piece of chocolate cake and Mitra’s blood-soaked body.")
    print("1 - Kitchen")
    print("2 - Corridor 5")
    cmdlist = ['1', '2', '3']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        kitchen()
    elif cmd == '2':
        cor5()

#hel
def ladder_bot():
    print("\n To the left is the storage room and to the right is the electrical hub")
    print("1 - Electrical hub")
    print("2 - Storage room")
    cmdlist = ['1', '2']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        print("The entrance to the electrical hub is blocked by the sliding door jamming on some storage boxes")
        print("There's a small gap but not nearly large enough for you to squeeze through")
        print("1 - Go back to ladder landing")
        if 'explosive' in inventory:
            print('2 - Use explosive to dislodge the boxes')
        cmdlist = ['1', '2']
        cmd = getcmd(cmdlist)
        if cmd == '1':
            ladder_bot()
        if cmd == '2':
            print("*crackling sound*")
            print("The oil is on fire, you quickly close the container and shove it in the gap")
            print("The sizzlings got louder")
            """add failure bomb ?"""
            time.sleep(1)
            print("--BOOM !--")
            time.sleep(2)
            """add random death ?"""
            print("Peaking your head out from the ladder chute")
            print("Fragments from the boxes scatter the area")
            """add item from boxes?"""
            print("The door is still jammed in place but there's a chunk missing")
            print("You crawl through")
            """alien accidentally killed by explosion"""
            alien['elec'] = False
            print(str(alien['elec']))
            elec_hub()
    elif cmd == '2':
        storage()

def storage():
    time.sleep(1)
    print("\n STORAGE UNIT")
    print("The expedition rover & shelves with repair supplies line up along the back wall")
    print("The door leading to the electrical hub can also be seen.")
    print("A trail of blood & bits runs from the door to a corpse lying flat on the ground")
    print("You can hardly recognise Marco’s corpse but the rotting banana in his hand gives him away.")
    print("He lies next to the 3D printer")
    print("You can see the lift from across the room")
    print("Life support systems, material supplies and oil reserve takes up the centre of the room.")
    print("1 - Lift")
    print("2 - Ladder up")
    print("3 - Electrical hub")
    print("4 - Fill up oil can")
    print("5 - Inspect 3D printer")
    cmdlist = ['1', '2', '3', '4','5']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        if power == True:
            lift()
        else:
            print("\nThe power is OFF. The emergency power is not enough to operate the lift")
            storage()
    elif cmd == '2':
        cor4()
    elif cmd == '3':
        elec_hub()
    elif cmd == '4':
        additem('oil')
        storage()
    elif cmd == '5':
        if power == False:
            print("Printer IDLE, emergency power mode ON")
            storage()
        elif power == True and 'cap_card' in inventory:
            print("--PERMISSION GRANTED--")
            print("Printing model w-747865. Estimated time: 30 seconds")
            time.sleep(6)
            print("80% Remaining")
            time.sleep(9)
            print("50% Remaining")
            time.sleep(9)
            print("20% Remaining")
            time.sleep(6)
            print("--PRINTING COMPLETE--")
            additem(gun)
            storage()
        elif power == True and 'cap_card' not in inventory:
            print("\n--PERMISSION NEEDED--")
            print("Model w-747865 needs clearance from ship Captain")
            storage()

def elec_hub():
    time.sleep(1)
    print("\n You enter the electrical hub of the ship.")
    print("You can see the main power supply and the backup generator.")
    print("A lift is on one side of the room while a ladder going up is on the other.")
    print("A door leading to the storage room can also be seen.")
    print("1 - Flip master power switch")
    print("2 - Lift")
    print("3 - Ladder up")
    print("4 - Storage room")
    cmdlist = ['1', '2', '3', '4']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        global power
        power == True
        print("\nThe main generator is now ON")
        print("Emergency battery is now OFF")
        elec_hub()
    elif cmd == '2':
        if power == True:
            lift()
        else:
            print("\nThe power is OFF. The emergency power is not enough to operate the lift")
            elec_hub()
    elif cmd == '3':
        cor4()
    elif cmd == '4':
        storage()

#asgard
def cor6():
    time.sleep(0.5)
    print("\n You are in the upper deck on a balcony overlooking the hub.")
    print("There are five rooms")
    print("1 - Control Room")
    print("2 - Ladder going down")
    print("3 - Lift")
    print("4 - Escape pod 1")
    print("5 - Escape pod 2")

    cmdlist = ['1', '2', '3', '4','5']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        if power == True:
            ctrl_room()
        else:
            print("Must construct additional Pylons !")
            print('The power is not on, Control Room door is LOCKED')
            cor6()
    elif cmd == '2':
        cor4()
    elif cmd == '3':
        if power == True:
            lift()
        else:
            print("The power is OFF. The emergency power is not enough to operate the lift")
            cor6()
    elif cmd == '4':
        esc1()
    elif cmd == '5':
        esc2()
def ctrl_room():
    time.sleep(0.5)
    print("\n You are now in the control room of the ship.")
    print("The communications panels lie to your left but seem damaged beyond repair.")
    print("The fuel injection and charging controls lie to your right.")
    print("Up ahead of you are the steering controls for the ship,")
    if 'cap_card' not in inventory:
        print("and lying on the floor next to a large open vent is your captain, Talha Jamal.")
        print("He looks seriously wounded.")
    print("1 - Approach fuelling and charging controls")
    print("2 - Enter vent")
    print("3 - Balcony")
    if 'cap_card' not in inventory:
        print("4 - Examine captain's body")
    cmdlist = ['1', '2', '3', '4']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        print("The fuelling controls appear to be working! You refueled the expedition ship.")
        global fuel
        fuel = True
        ctrl_room()
    elif cmd == '2':
        print("You enter the vent and begin to crawl through it when you hear a growl which reverberates throughout the vent.")
        time.sleep(2.5)
        print("*Screeching noises*")
        dead()
    elif cmd == '3':
        cor6()
    elif cmd == '4':
        time.sleep(1.5)
        print("Captain TJ is dead. You see his keycard and decide to take it.")
        additem("cap_card")
        ctrl_room()
def esc1():
    print("\n The first escape pod seems to be missing.\nI wonder where it is ?")
    cor6()
def esc2():
    print("\n The second escape pod is available. There's a trail of blood leading to the hatch door.")
    print("1 - Open the pod")
    print("2 - Return to the upper deck")
    cmdlist = ['1', '2']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        esc2_in()
    elif cmd == '2':
        cor6()
def esc2_in():
    print("The door pop open")
    time.sleep(2)
    print("A stench of blood")
    time.sleep(2)
    print("A thing-Something is on the floor")
    #needs fixing
#Lift
def lift():
    print("\n You arrive at the lift")
    print("Which floor?")
    print("1 - Upper Floor")
    print("2 - Main Area")
    print("3 - Lower Floor")
    cmdlist = ['1', '2','3']
    cmd = getcmd(cmdlist)

    if cmd == '1':
        cor6()
    elif cmd == '2':
        cor2()
    elif cmd == '3':
        ladder_bot()

#interaction
def additem(item):
    inventory.append(item)
    print("\n > "+item + " added to INVENTORY")
    time.sleep(0.75)
    print('\nYou are still in the :')
    time.sleep(0.5)
def getcmd(cmdlist):
    cmd = input().strip().lower()
    if cmd in cmdlist:
        return cmd
    elif cmd == 'help':
        print('\nTYPE: inventory to view items')
        print('craft to craft items')
        print('or quit to suicide')
        return getcmd(cmdlist)
    elif cmd == 'inventory':
        print('\n inventory contains:\n')
        for item in inventory:
            print('-- %s' % (item))
        return getcmd(cmdlist)
    elif cmd == 'craft':
        print("Recipe book")
        for dish, code in recipe.items():
            print('--' + dish + ' : ' + str(code))
        make = input("Type crafting code\n")
        if make == '2006':
            explosive()
        elif make == '2243':
            acid()
        elif make == '6363':
            memes()
        else:
            print("You toss ingredients around aimlessly and hurt yourself in the process")
            print("Who did you think you are ? Ratatouille ?")
            time.sleep(0.75)
        return getcmd(cmdlist)
    elif cmd == 'quit':
        print("\nGoodbye cruel world")
        dead()
    else:
        print('\n error. invalid command-\n')
        return getcmd(cmdlist)
def explosive():
    if (all(x in inventory for x in ['container','fertiliser','oil','battery'])) == True:
        inventory.remove('container','fertiliser','oil')
        time.sleep(0.5)
        print("Hmmm ...Fertiliser is a good source of ammonium nitrate")
        print("Oil would kick start the detonation")
        print("The lithium-oxigen reaction from the battery could be used as a primer")
        time.sleep(1)
        additem(explosive)
    else:
        print("\nYou don't have the items needed to make this\n")
        time.sleep(0.75)
def acid():
    if all(x in inventory for x in ['mold', 'water']) == True:
        inventory.remove('mold','water')
        additem(acid)
    else:
        print("\nYou don't have the items needed to make this\n")
        time.sleep(0.75)
def memes():
    print("Hah, making memes in 3018")
    time.sleep(0.75)
#endgame
def dead():
    time.sleep(0.5)
    print("\n*darkness*")
    time.sleep(2)
    print("\nYOU DIED.\n")
    time.sleep(2)
    exit()
def victory():
    time.sleep(2)
    print("\nYou've done it! You survived and managed to make your way off the ship! It's smooth sailing from here on out... hopefully.")
    time.sleep(3)
    exit()
start()
