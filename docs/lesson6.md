##Lesson 6: Functions
So far, we have covered the basics of Python. Variables, data types, lists, loops, control structures, dictionaries. But now it's time for us to start creating our own functions, so that we can make more complex programs.

What is a function? A **function** is basically something that takes in an input and produces and output. In programming, we use functions to do all sorts of different things. The question here is, how do we make functions in Python?

Let's say we want to print out someone's name. Let's create a function that does that. In Python, the structure of a basic function is as follows. 

	def functionname( parameters):
		body
		return 
Let's break this down. The first word def, is a keyword in Python. When Python sees this word it knows that we are about to define a function. The 'functionname' can be whatever we want it to be. For a function to print someone's name, we might call the funciton printname. The 'parameters' are the input for the function. We can pass in parameters into a function, and then the function can use those parameters and give us an output. The 'body' is the code that would do whatever we want the function to do. The return, is what we use to return the output. If we do not have anything to return, we can simply just put return. Let's try making that printname function.

	def printname( str ):
	print(str)
	return 
Now, once we make a function, we need to call it. Calling a function basically means telling Python that we want to use it. Let's say I want to print out Tom's name using this function. 

	printname('Tom')
I would type out the funciton and pass in the parameter, which in this case is a string, 'Tom'. 

An important thing to remember is that parameters are passed in by reference. What that means is, is that the value of the actual parameters will change if we pass it into the function. Let's look at an example. Let's say we have a list of numbers. We want to create a function that will add more numbers to a list. 

	def addNum ( numList)
	numList.append([5, 6, 7, 8])
	print("Current vals", numList)
	return
Let's try calling the function.

	numList = [1, 2, 3, 4]
	addNum(numList) 
	print("Current vals", numList)
This is what will print out.

	Current values [1, 2, 3, [5, 6, 7, 8]]
	Current values [1, 2, 3, [5, 6, 7, 8]]
If we wanted to make sure that that reference didn't change, then we would have to create another reference inside our function.

	def addNum ( numList)
	numList = [5, 6, 7, 8]
	print("Current vals", numList)
	return
Let's try calling the function.

	numList = [1, 2, 3, 4]
	addNum(numList) 
	print("Current vals", numList)
This is what would print out.

	Current values [1, 2, 3, 4]
	Current values [5, 6, 7, 8]
	