# code-to-convert-binary-numbers
'''Create a program that converts X, an integer (in base 10) to a binary number (in base n), where X and n are integers entered by the user. 
The program then displays the solution in the form:
➖➖➖➖➖➖➖➖➖➖➖
3 | 7
   | 2 r 1
   | 0 r 2
:. 7 base 10 = 21 base 3
➖➖➖➖➖➖➖➖➖➖➖'''
rem = []
num = int(input("Enter number in Base 10 : "))
Base = int(input("Enter the base: "))

n = Base
X = num

print(" ")
print(n, "|", X)
while X >= 1:
    rem.append(X % n)
    print(n, "|", X//n, "r", X % n)
    X = X//n

rem.reverse()
output = "".join(str(e) for e in rem)
print(":.",num,"in base 10 =" ,output,"in base",n)
