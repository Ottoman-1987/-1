# -1
Мой первый репазиторий
#Игра по угадыванию чисел
import  random

guessesTaken = 0

print('Привет! как тебя зовут?')
myName = input()

number = random.randint(1, 2)
print('Что ж, ' + myName + ', Я загадываю число от 1 до 2.')

for guessesTaken in range(6):
    print('Попробуй угадать.')# 4 пробела перед именем функции print
    guess = input()
    guess = int(guess)

    if guess < number:
        print('Твое число слишком маленькое.')# 8 пробелов перед именем функции print

        if guess > number:
            print('Твое число слишком большое.')

            if guess == number:
                break

if guess == number:
    guessesTaken = str(guessesTaken + 1)
    print('Отлично,' + myName + '! Ты справился c ' + guessesTaken + ' попытки!' )

if guess != number:
    number = str(number)
    print('Увы, Я загадала число ' + number + '.')

