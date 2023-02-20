# Python-GradeCal
import sys

#function used for error handeling.
def user(msg,less,more):
    while True:
        try:
            enter=float(input(msg))
        except ValueError:
            print("Enter number between : ", less, "and", more)
            continue
        if enter < less or enter > more:
            print("Enter number between :", less, "and", more)
        else:
            return enter

#calculating total and average.
def CalcAverage(m1, m2, m3, m4):
    #This function calculate the total marks average
    total = (m1 + m2 + m3 + m4)
    average = total/4
    return average    
    
#user input statement.
entry = int(user("How many student grade's do u want to enter? : ",1,sys.maxsize)) 

for value in range(entry):
        
        #input for student name and 4 subject marks.
        std= str(input("Enter Student Name: "))
        m1 = user("Enter Marks 1: ",1,100)
        m2 = user("Enter Marks 2: ",1,100)
        m3 = user("Enter Marks 3: ",1,100)
        m4 = user("Enter Marks 4: ",1,100)
        
        #print of student name.
        print("\n")
        print("Student Name: ",std)
        
        #Print average of total 4 subjects.
        ave = CalcAverage(m1,m2,m3,m4)
        print("Average Marks: ", ave)
        
        #Condition check for Grades and Status.
        if(ave >= 90 and ave <= 100):
            print("Student Grade: A+")
            print("Student Status: Pass")
        elif(ave >=80 and ave < 90):
            print("Student Grade: B+")
            print("Student Status: Pass")
        elif(ave >= 70 and ave < 80):
            print("Student Grade: B")
            print("Student Staus: Pass")
        elif(ave >= 60 and ave < 70):
            print("Student Garde: C")
            print("Student Status: Pass")
        else:
            print("Student Grade: F")
            print("Student Status: Fail")
