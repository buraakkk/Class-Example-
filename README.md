# Class-Example-

import matplotlib.pyplot as plt


# Create a class Circle

class Circle(object):
    
    # Constructor
    def __init__(self, radius=3, color='blue'):
        self.radius = radius
        self.color = color 
    
    # Method
    def add_radius(self, r):
        self.radius = self.radius + r
        return(self.radius)
    
    # Method
    def drawCircle(self):
        plt.gca().add_patch(plt.Circle((0, 0), radius=self.radius, fc=self.color))
        plt.axis('scaled')
        plt.show()  
        
        
RedCircle = Circle(2, 'red')

#print(RedCircle.drawCircle())




class Rectangle(object):
    
    # Constructor
    def __init__(self, width=2, height=3, color='r'):
        self.height = height 
        self.width = width
        self.color = color
    
    # Method
    def drawRectangle(self):
        plt.gca().add_patch(plt.Rectangle((0, 0), self.width, self.height ,fc=self.color))
        plt.axis('scaled')
        plt.show()



SkinnyBlueRectangle = Rectangle(5, 3, 'red')
print(SkinnyBlueRectangle.height)       
print(SkinnyBlueRectangle.width)
print(SkinnyBlueRectangle.color)


SkinnyBlueRectangle.drawRectangle()
