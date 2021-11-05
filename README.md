#   HEALTH MANAGEMENT SYSTEM
#   3 clients Harry, Rohan, Hammad


def getdate():
    import datetime
    return datetime.datetime.now()
#   Total 6 files
#   write a function that when executed takes as input client name
#   one more function to retrieve exersise or food for any client

def getname1():
    a = int(input("Enter 1 for retriving data for Harry \n"
                  "Enter 2 for retriving data for Rohan \n"
                  "Enter 3 for retriving data for Hamaad \n"))
    return a
def getname2():
    e = int(input("Enter 1 for writing data for Harry \n"
                  "Enter 2 for writing  data for Rohan \n"
                  "Enter 3 for writing data for Hamaad \n"))
    return e

def retrivingdata():
    a = getname1()
    b = int(input("Enter 1 if you want to retrieve the data of food \n"
                  "Enter 2 if you want to retrieve the data of exercise \n"))
    if (a==1):
        if (b==1):
            with open("Harry_food.txt") as f:
                d = f.read()
                print("\n")
                print("[",getdate(),"]", d , end=" ")
        else:
            with open("Harry_exercise.txt",) as f:
                d = f.read()
                print("\n")
                print("[", getdate(), "]", d , end=" ")
                print("\n")
    elif (a==2):
        if(b==1):
            with open("Rohan_food.txt") as g:
                d = g.read()
                print("\n")
                print("[", getdate(), "]", d , end=" ")
        else:
            with open("Rohan_exercise.txt") as g:
                d = g.read()
                print("\n")
                print("[", getdate(), "]", d , end=" ")
    else:
        if(b==1):
            with open("Hammad_food.txt") as h:
                d = h.read()
                print("[", getdate(), "]", d , end=" ")
        else:
            with open("Hammad_exercise.txt") as h:
                d = h.read()
                print("\n")
                print("[", getdate(), "]", "\n" ,d , end=" " )
    return 0
def writedata():
    e = getname2()
    f = int(input("Enter 1 if you want to add food data \n" 
                  "Enter 2 if you want to adding the data of exercise \n"))
    if(e==1):
        if(f==1):
            print("Enter the food you have eaten\n")
            z = open("Harry_food.txt","a")
            z.write(input())
            z.close()
        else:
            print("Enter the exercise you have done\n")
            with open("Harry_exercise.txt", "a") as z:
                z.write(input())
    elif (e==2):
        if(f==1):
            print("Enter the food you have eaten\n")
            with open("Rohan_food.txt", "a") as z:
                z.write(input())
        else:
            print("Enter the exercise you have done\n")
            with open("Rohan_exercise.txt", "a") as z:
                z.write(input())
    else:
        if(f==1):
            print("Enter the Food you have eaten\n")
            with open("Hammad_food.txt", "a") as z:
                z.write(input())
        else:
            print("Enter the exercise you have done\n")
            with open("Hammad_exercise.txt", "a") as z:
                z.write(input())
    print("Do you want to write about more peoples? (y/n) \n")
    x = input()
    if (x.lower()=="y"):
        writedata()
    else:
        print("Do you want to retrieve any data??(y/n) \n")
        w = input()
        if (w.lower() == "y"):
            retrivingdata()
        else:
            print("THANK YOU FOR VISITING")
k = int(input("Enter 1 if you want to retrieve data \n"
              "Enter 2 if you want to write in the data \n"))
if (k==1):
    c = retrivingdata()
else:
    j = writedata()
