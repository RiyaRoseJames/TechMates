from hangman_stage import hangman    
import random

def guess_a_word():                           #defining a function for a word randomly choosen from the word list
    word=random.choice(list_words)
    return word
    print("Guess the programming word")


def letter_is_present(letter):                #defining a function to check the presence of a letter given by user in the word to be guessed
    if letter.lower() in word.lower():
      return letter.lower()
    else: 
      return False


def fill_dash(letter):                        #defining a function to fill the dashes with the letters that matches with the guessing word
  global blank_dash,word
  blank_dash= list(blank_dash)
  for i, l in enumerate(word):
    if letter==l:
      blank_dash[i]=letter
  print("".join(blank_dash))



def display_hangman():                        #defining a function to display hangman stages if letter is guessed wrong
  global chances_given
  chances_given +=1
  print(hangman[chances_given])



def check_the_letter(user_choice):            #defining a function either to fill the dash(if guessed correct)or to display hangman stages
    letter =letter_is_present(user_choice)  
    if letter:
      fill_dash(letter)
    else:
      display_hangman()



def check_the_word(user_choice):             #defining a function to check when the user inputs a guesssed word(as a whole)matches the correct word
   if user_choice.lower() ==word.lower():
     return True
   else:
    return False


#main body

chances_given=0
win=False

list_words=['python','java','html','flutter','javascript','git','swift','php']
word=guess_a_word()
blank_dash='_'*len((word))/print(blank_dash) 
print(hangman[0])


while chances_given <=5 and not win:           #no of opportunities will be 6 ,after which user will lose
     user_choice= input()
     if len(user_choice)==1:                   #to check the user input
         check_the_letter(user_choice)
     else:
        win= check_the_word(user_choice)
        break
      

if '_' not in blank_dash:
  win=True


#to print the result
if win:
  print("win!!")
else:
  print("Lost!")
