import turtle

def quadratic_function(x, a, b, c):
    return a * x**2 + b * x + c

def draw_quadratic_function(a, b, c):
    screen = turtle.Screen()
    screen.setworldcoordinates(-10, -10, 10, 10)
    t = turtle.Turtle()
    t.speed(0)
    t.penup()
    t.goto(-10, 0)
    t.pendown()
    t.goto(10, 0)
    t.penup()
    t.goto(0, -10)
    t.pendown()
    t.goto(0, 10)
    t.penup()
    t.goto(-10, quadratic_function(-10, a, b, c))
    t.pendown()
    for x in range(-100, 101):
        x = x / 10
        t.goto(x, quadratic_function(x, a, b, c))

    screen.mainloop()
