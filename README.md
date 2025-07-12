# python13
function in function

#function in function
def outer():
    print("outer")
    def inner():
        print('inner')
    inner()
outer()

#cal using function
def cal(a,b):
    def add():
        return a+b
    def sub():
        return a-b
    def mul():
        return a*b
    def div():
        return a/b
    def squ():
        return a**b
    print("Addition",add())
    print("Subtraction",sub())
    print("Multiplicatilon",mul())
    print("Division",div())
    print("Square",squ())
a=int(input("Enter a number1"))
b=int(input("Enter a number2")) 
cal(a,b)


#What is the role of the return greeter statement in the greet_person function?
def greet(text):
    def inner(name):
        return f"{text} {name}!"
    return inner
hi= greet("Hello")
print(hi("Abhi"))
