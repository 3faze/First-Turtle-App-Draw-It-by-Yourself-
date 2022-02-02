```
#Import Libraries
import turtle as t
import time as ti

#Screen
screen = t.Screen()
screen.title("Turtle App1(Draw It)")
screen.screensize(300, 600)
screen.bgcolor("steel blue")
screen.tracer(0)

#Border
border = t.Turtle()
border.hideturtle()
border.speed(0)
border.color("white")
border.penup()
border.setposition(-350, -350)
border.pensize(3)
border.pendown()
border.showturtle()

#Lines of the border
for sides in range(4):
	border.fd(700)
	border.lt(90)
border.hideturtle()

#Making a title appear on top of the page
pagetitle = t.Turtle()
pagetitle.hideturtle()
pagetitle.speed(0)
pagetitle.color("white")
pagetitle.penup()
pagetitle.setposition(0, 270)
pagetitle.showturtle()
pagetitle.shapesize(4)
pagetitle.write("Draw It By Yourself!", align = "center", font = ("Comic Sans MS", 34, "normal"))
pagetitle.hideturtle()


#Making a button
button = t.Turtle()
button.hideturtle()
button.setposition(0, 0)


#Making the controlable line
mainline = t.Turtle()
mainline.hideturtle()
mainline.speed(0)
mainline.color("white")
mainline.penup()
mainline.setposition(0, 0)
mainline.pensize(3)

def line_fd():
	mainline.pendown()
	mainline.fd(50)

def line_up():
	mainline.pendown()
	mainline.right(90)
	mainline.fd(50)

def line_lf():
	mainline.pendown()
	mainline.left(90)
	mainline.fd(50)

t.listen()
t.onkeypress(line_fd, "w")
t.onkeypress(line_up, "d")
t.onkeypress(line_lf, "a")


#Main Loop
#Here I set run to True so i can break a nested loop
run = True
while run:
	screen.update()



turtle.exitonclick()
```
