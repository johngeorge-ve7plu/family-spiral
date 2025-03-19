# family-spiral

import turtle
t = turtle.Pen()
t.speed(0)
colors = ["blue","red","blue" ,"gold","purple","pink"]

# Getting the input from the user
name = input("Enter your family name: ")

family = []

while name != "":
    name = input("Enter your family name: ")
    family.append(name)

for x in range(100):
    t.pencolor(colors[x%len(family)])
    t.penup()
    t.forward(x*4)
    t.pendown()
    t.write(family[x%len(family)])
    t.left(360/len(family)+2)

turtle.done()
