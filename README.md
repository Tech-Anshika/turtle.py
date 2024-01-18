# turtle.py
This is my 2nd git repository (using turtle)
The provided Python code utilizes the Turtle graphics library to create a visually appealing recursive tree. Here's a description of the code:
Library Import:
import turtle ->This line imports the 'turtle' module, which provides a convenient way to draw graphics using a turtle metaphor.
Turtle Initialization:
tu = turtle.Turtle() -> A turtle object named 'tu' is created to draw on the screen.
Setting up Turtle Screen:
tu.screen.bgcolor("black") ->The background color of the turtle screen is set to black.
Turtle Appearance Settings:
tu.pensize(2)
tu.color("green")
tu.left(90)
tu.backward(100)
tu.speed(100)
tu.shape('turtle')
These lines configure the turtle's pen size, color, orientation, initial position, drawing speed, and shape.
Recursive Tree Drawing Function:
def tree(i):
    if i < 10:
        return
    else:
        tu.forward(i)
        tu.color("orange")
        tu.circle(2)
        tu.color("brown")
        tu.left(30)
        tree(3 * i / 4)
        tu.right(60)
        tree(3 * i / 4)
        tu.left(30)
        tu.backward(i)
The tree function is defined to draw a recursive 'tree'. It takes a parameter 'i' representing the length of the branch. If 'i' is less than 10, the function returns, otherwise, it draws a branch, a circle as a leaf, and recursively calls itself to draw the left and right sub-trees.
Drawing the Tree:
tree(100) -> The 'tree' function is called with an initial length of 100 to start drawing the entire tree.
Finishing the Drawing:
turtle.done()
