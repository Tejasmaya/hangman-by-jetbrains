# hangman by jetbrains
 a CLI game



# # Write your code here
# import random
# import re
# 
# from copy import copy
# 
# list_ = ["python", "java", "swift", "javascript"]
# choice = copy(random.choice(list_))
# lost = 0
# won = 0
# 
# print(f'''
# H A N G M A N  
# ''')
# 
# 
# def play():
#     global lost
#     global won
#     attempts = 8
#     printout = ('-' * (len(choice)))
#     print(printout)
#     s = [*printout]
#     guessed = set()
#     while attempts != 0:
#         # print(printout)
#         # print(attempts)
#         # print(choice)
#         letter = input('Input a letter:')
# 
#         if letter in choice and letter not in s and letter not in guessed \
#                 and letter.isalpha() and len(letter) == 1 and letter.islower():
#             indices = [i.start() for i in re.finditer(letter, choice)]
# 
#             for i in range(len(choice)):
#                 if i in indices:
#                     s[i] = letter
#             printout = ''.join(s)
#             print('\n', printout)
# 
#         elif len(letter) != 1:
#             print('Please, input a single letter.')
#             print('\n', printout)
# 
#         elif not letter.islower() or not letter.isalpha():
#             print('Please, enter a lowercase letter from the English alphabet.')
#             print('\n', printout)
# 
#         elif letter in guessed:
#             print("You've already guessed this letter.")
#             print('\n', printout)
# 
#         elif letter in s:
#             print("No improvements.")
#             print('\n', printout)
#             attempts -= 1
# 
#         else:
#             print("That letter doesn't appear in the word.")
#             attempts -= 1
#             if attempts == 0 and printout != choice:
#                 print('You lost!')
#                 lost += 1
# 
#                 menu()
#                 break
#             print('\n', printout)
#         guessed.add(letter)
#         if printout == choice:
#             print(f'You guessed the word {choice}!')
#             print('You survived!')
#             won += 1
# 
#             menu()
#             break
#         # if attempts == 0 and printout != choice:
#         #     # print(attempts)
#         #     print('You lost!')
#         #     # print('Thanks for playing!')
# 
# 
# def menu():
#     ans = input('Type "play" to play the game, "results" to show the scoreboard, and "exit" to quit:')
#     if ans not in ["play", "results", "exit"]:
#         menu()
#     elif ans == 'play':
#         play()
#     elif ans == "exit":
#         pass
#     elif ans == "results":
#         print(f'''
# You won: {won} times.
# You lost: {lost} times.''')
#         menu()
# 
# 
# menu()

