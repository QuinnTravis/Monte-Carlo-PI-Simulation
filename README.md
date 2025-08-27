# Monte-Carlo-PI-Simulation
Simulate value of pi, using ratio of square and circle in 2D and 3D
import math
import random

interval = int(input("Enter Number of points you would like ")) 
dimension = input("Enter Dimension you would like to choose ")

in_circle = 0


if (dimension.lower() == '2d' ):
    for i in range(interval):
        x=random.random()
        y=random.random()
        r=math.sqrt(x**2+y**2)
        
        if r<=1:
            in_circle += 1

    print("The estiamted value of pi is: " + str(4*(in_circle/interval)))
    
    
elif (dimension.lower() == '3d' ):
    for i in range(interval):
        x=random.random()
        y=random.random()
        z=random.random()
        r=math.sqrt(x**2+y**2+z**2)
        
        if r<=1:
            in_circle += 1
        
            
    print("The estiamted value of pi is: " + str(6*(in_circle/interval)))
