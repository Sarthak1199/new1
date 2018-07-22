#HANGMAN THE GAME
import random

words=[]
r=input("You want to play with how many words?")
for i in range(int(r)):
    words.insert(i,input("Input word"))

chosen_word=random.choice(words)
print (chosen_word)
#for i in range(0,len(chosen_word)):
    #print (chosen_word[i])
print ("Let's start the game!")
print ("1 letter at a time. 3 strikes and you're out")
strikes=1   #No. of strikes
length=0

while strikes<=3:
    print (end='\n')
    letter = input("Guess away!")  #Guessed letter
    flag = 0
    for i in range(0,len(chosen_word)):
        if(letter==chosen_word[i]):
            flag=1
            length+=1
            print (letter,end=" ")
        else:
            print ("_",end=" ")
    if(flag==0):
        strikes=strikes+1
        print ("You messed up!")
    if (length==len(chosen_word)):
        print (end='\n')
        print ("Hurraay! You did it.")
        break







