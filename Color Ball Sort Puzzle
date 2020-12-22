# Defining variables and lists
b = "Blue"
y = "Yellow"
g = "Green"

panel1 = [b,g,y,b]
panel2 = [b,g,y,y]
panel3 = [g,y,b,g]
panel4 = []
panel5 = []

# Printing initial display messages
print("Welcome!")
print("Panel 1:",panel1)
print("Panel 2:",panel2)
print("Panel 3:",panel3)
print("Panel 4:",panel4)
print("Panel 5:",panel5)
print("Instructions:")
print("*Sort these balls into different panels according to their colors by moving the first ball of any panel to an empty panel or over the balls of any other panel.")
print("*You can only access the top-most balls of the panels.")
print("*You can only put like colored balls on top of each other. A move is valid only if the color of top-most balls is same or if the final panel is empty.")
print("*There cannot be more than four balls in any panel.")
print("*For each move enter the initial and final positions by pressing enter after each input. The inputs are integers between 1 to 5.")
print("*Here initial position means the numbered value of the panel you want to select the ball from and the final position refers to the numbered value of the panel you want to put the ball in.")
print("*PLEASE ENTER INTEGER VALUES ONLY.")

# Defining function for moves
def move(initial_position,final_position):

    # Defining dictionary for easy access to panels
    d = {1:panel1, 2:panel2, 3:panel3, 4:panel4, 5:panel5}

    if initial_position in range(1,6):
        l1 = d[initial_position]

        if final_position in range(1,6):
            l2 = d[final_position]

            if len(l2) >= 4:
                print("Panel Full!")
                print("Invalid Move. Try again.")
            else:
                if l2 == []:
                    l2.insert(0,l1[0])
                    del(l1[0])
                elif l1[0] == l2[0]:
                    l2.insert(0,l1[0])
                    del(l1[0])
                else:
                    print("Invalid Move")
                    print("Different colors! Try again.")

        else:
            print("Invalid Input")
            print("Input should be a number from 1 to 5.")

    else:
        print("Invalid Input")
        print("Input should be a number from 1 to 5.")

# Code for execution of every move
variable_to_check_if_all_sorted = 0
variable_to_run_the_while_loop = 0
number_of_moves = 0
while variable_to_run_the_while_loop == 0:
    variable_to_check_if_all_sorted = 0
    try:
        move(int(input("Enter initial position: ")),int(input("Enter final position: ")))
        number_of_moves = number_of_moves + 1
        for i in [panel1,panel2,panel3,panel4,panel5]:
            if len(i) == 0 or len(i) == 4:
                if len(set(i)) == 0 or len(set(i)) == 1:
                    variable_to_check_if_all_sorted = variable_to_check_if_all_sorted + 1
            if variable_to_check_if_all_sorted == 5:
                variable_to_run_the_while_loop = 1
                print("Cheers!")
                print("Balls Sorted.")
                print("Number of moves taken:",number_of_moves)
                break
    except:
        print("Invalid input.")
        print("Input must be an integer.")

    # Printing all panels after each move
    print("Panel 1:",panel1)
    print("Panel 2:",panel2)
    print("Panel 3:",panel3)
    print("Panel 4:",panel4)
    print("Panel 5:",panel5)
