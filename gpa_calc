def gpa(grade, level): # finds the grade point for each grade with it's corresponding level
  level = level.lower() # sets it to lowercase
  accept = ['k', 'h', 'ap', 'dc'] # levels that will add 1 point to the base gradepoint
  if grade >= 90 and grade <= 100: 
    point = 6
  elif grade >= 80 and grade <= 89:
    point = 5
  elif grade >= 75 and grade <= 79:
    point = 4
  elif grade >= 70 and grade <= 74:
    point = 3
  elif grade >= 0 and grade <= 69:
    point = 0
  if level in accept and grade >= 70: # adds 1 to the point if its a K level or higher class & not a 0 point class (above a 69)
    point += 1
  return point

def avg(class_num, grades_lst, level_lst):
  total = 0 # sets 0 for the total
  
  for i in range(class_num): # how many classes (also defines which grade & level goes into GPA function
    total += gpa(grades_lst[i], level_lst[i])
  
  return total / class_num # finds the actual GPA

def main():
  level = [] #empty list for the levels
  grades = [] #same for grades
  classes = 0 # how many classes

  while True: #loops until done == y
    while True:
      grad = input('What grade do you have?: ')
      if grad.isdigit(): #checks if the grade is a number
        grad = int(grad) # makes it an integer
        if grad >= 0 and grad <= 100: #checks if its actually a valid grade
          break
        else:
          print('\nInvalid input. Please input a number 0 - 100\n') #error messages
      else:
        print('\nInvalid input. Please input a number 0 - 100\n')
    grades.append(grad) #adds the grade to the list

    while True: #same ordeal with the levels
      acc = ['l', 'k', 'h', 'ap', 'dc']
      lev = input('\nWhat level is the class?: ')
      if lev.lower() in acc:
        break
      else:
        print('Invalid input. Please input L, K, H, AP, or DC.')
    level.append(lev)

    classes += 1 # will be used to divide total gradepoints

    while True: # loop for a correct answer if done or not
      done = input('\nDone? y/n: ')
      if done.lower() == 'y' or done.lower() == 'n':
        break
      else:
        print('Invalid input. Please input either "y" or "n".')
    if done == 'y':
      break
    print() # makes a space after the loop

  print('\nYour GPA is', round(avg(classes, grades, level),3)) # rounds the gpa to the 3rd decimal

main() # calls main
