import random

print("欢迎来到猜数字游戏！")
print("我已经想好了一个1到100之间的整数，请猜一下它是多少。")

number = random.randint(1, 100)
guess = None
guess_count = 0

while guess != number:
    guess = int(input("请输入你的猜测："))
    guess_count += 1
    
    if guess < number:
        print("你猜的数字太小了，请再试一。")
    elif guess > number:
        print("你猜的数字太大了，请再试一次。")
    else:
        print("恭喜你，你猜对了！")
        print("你一共猜了{}次。".format(guess_count))
