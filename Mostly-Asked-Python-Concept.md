### List vs Tuple
#### List
- List are mutable
- they are container to store different types of objects . They are used to iterate objects.
- Syntax of List :
  
      list = ['a', 'b', 1, 3, 4]
  
- The iterartion performed in list is comparetively slower than tuple.
- Insertion , deletion operation can be performed better.
- It consume more memory.
  
#### Tuple
- tuple are immutable.
- tuple are container that store different type of immutable objects.
- Syntax of tuple :
  
     tuple = ( 'a', 'b', 1, 2, 3)
     
- it consume less memory
- iteration is processed faster.
- element can be accessed faster.


### Decorator
Decorator is a function that take another function as an argument, add some functionality in it and returns a thrid function. Without making changes to the source code of the function that is passed as an parameter.

 Example :  
 
      #the decorator function that take func as argument here it is show function, then add functionality and return wapper function 
      def decorator_func(func):
          def wapper_func():
              print("wapper function")
              return func()
          print("decorator function")
          return wapper_func
      
      #it the function which we will pass as argument
      def show():
          print("show function")
          
      decorator function call  
      decorator_show = decorator_func(show)
      decorator_show()
      
      #Another way of calling decorator function
      @decorator_func
      def display():
          print("display function")
          
      display()

### List comprehension vs Dictionary comprehension
comprehension means the expression , which is executed for each element along with the for loop to iterate over each element

#### List Comprehension
Syntax :
      [expression **for** item **in** iterable **if** condition]

Example : 

      #Comman way :
      ls = []
      for i in range(10):
         if i%2:
            ls.append(i*i)
   
      #Using List comprehension
      ls = [i*i for i in range(10) if i%2]
      print(ls)

Output : [1, 9, 25, 49, 81]

#### Dict Comprehension
Syntax :
      {key : value **for** (key,value) **in** iterable **if** condition }

Example :

      #common way 
      d = {}
      for n in range(10):
         if n%2:
            d[n]=n*n
      print(d)

      #using dict comprehension
      d = {n:n*n for n in range(10) if n%2}
      print(d)

Output : {1:1, 3:9, 5:25, 7:49, 9:81}


### How to manage memory in python ?
- In python, we have private heap for storing python objects and data structures.
- Interpreter takecare of python heap and programmer has no access to it.
- The allocation of heap space to python object is done by python memory manager.
- Python core APIs provide some tools to programmer for code reliable and robust program.
- python garbage collector recycle the unused memort. The python object which is no longer referenced by the python program is determined by it. the memory occupied by python object is freed and Make it available to heap space.
- the gc module functions are used to enable/disable the pytho garbage collector:
     gc.enable() : Enable the automatic garbage collection.
     gc.disable() : Disable the automatic grabage collection.
  
   
