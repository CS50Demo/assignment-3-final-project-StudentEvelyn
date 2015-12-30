# Problem Set 3
Third assignment in CS50

What does the following code print?

<pre><code>
import pylab
xVals = pylab.arange(0, 10)
yVals = 2*pylab.arange(0, 10)
a, b = pylab.polyfit(xVals, yVals, 1)
print round(a)
print round(b)
</code></pre>

Assume that G is a Digraph in which each node represents a city (i.e., n.getName() returns the name of a city), and the weight of each edge the cost of flying nonstop between pairs of cities.
Write a function that meets the specification below.

<pre><code>
def cheapestTrip(city1, city2, G):
 """Assumes that city1 and city2 are strs.
 Returns the cost of the least expensive way to fly round trip
 between city1 to city2.
 If no such path exists (e.g., because there
 is no node corresponding to city2), it returns None."""
</code></pre>

What does the following code print? 

<pre><code>
class Shape(object):
 def __eq__(s1, s2):
 return s1.area() == s2.area()
 def __ge__(s1, s2):
 return s1.area() >= s2.area()
class Square(Shape):
 def __init__(self, h):
 self.side = float(h)
 def area(self):
 return self.side**2
 def __str__(self):
 return 'Square with side ' + str(self.side)
class Circle(Shape):
 def __init__(self, radius):
 self.radius = radius
 def area(self):
 return 3.14159*(self.radius**2)
 def __str__(self):
 return 'Circle with radius ' + str(self.radius)
def f(L):
 if len(L) == 0: return None
 x = L[0]
 for s in L:
 if s >= x:
 x = s
 return x
s = Square(4)
print s.area()
L = []
shapes = {0:Circle, 1: Square}
for i in range(10):
 L.append(shapes[i%2](i))
print L[4]
print f(L)
</code></pre>
