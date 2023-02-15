```python
# 1.Explain why we have to use the Exception class while crating a custom Exception.
# Ans-
#     In python,the built-in'Exception'class is the base class for all exceptions. when we create a custom exception,we usually want it to behave like a standard exception and be compatible with the existing exception handling mechanism in python.To achieve this,we need to inherit our custom exception class from the'exception' class.
    
#     By inheriting from the 'exception'class our custom exception inherits all the functionality of base class,such as the ability to print a traceback,get a message string,and interact with other exceptions.This allows us to use our custom exception in the same way as the built-in exceptions,with the same 'try-except'block syntax.
    
#     in addition,by inheriting from the'Exception' class,we can make use of the built-in exc
```


```python
# 2.Write a program to print python Exception Hierarchy.
# Ans-
#      import sys
    
#     def print_exception_hierarchy(exc):
#         print(type(exc))
#         for subclass in exc.__subclasses__():
#             print_exception_hierarchy(subclass)
            
#     print_exception_hierarchy(BaseException)
```


```python
# 3.What errors are defined in the ArithmeticError class? Explain any two with an example.
# Ans-
#    The 'ArithmeticError' class is a built-in exception class in python that serves as a base class for all exceptions that occure during arithmetic operations.It is a subclass of the 'exception'class and itself the parent class for several more specific arithmetic-related exception classes.
    
#     1."ZeroDivisionError":
#           This exception is raised when we try to divide a number by zero.
        
#         for example:
#                      a = 10
#                      b = 0
#             try:
#                      c = a / b
#             except ZeroDivisionError:
#                     print("Error cannot divide by zero")
                    
#     2."OverflowError":
#            This exception is raised when a calculation exceeds the maximum representable value for a numerical type
        
#         for example:
#                      import sys 
#                      a = sys.maxsize
#                     try:
#                         b = a * a
#                     except OverflowError:
#                            print("Error:Result too large to represents as a number")
                            
# overall,The "ArithmaticError"class and its derived exceptions are useful for handling errors tha
```


```python
# 4.Why LookupError class is used? Explain with an example KeyError and IndexError.
# Ans-
#      The "LookupError" class is a built-in exception class in python that serves as a base class for all exceptions that occure when a key or index not found during a lookup operation.It is a subclass of the "Exception"class and its itself the parent class for several more specific lookup-related exception classes.
    
#     1.KeyError- This exception is raised when a dictionary key is not found in the dictionary.
    
#      for example :
#                    my_dict = {'a': 1, 'b' : 2 ,'c' : 3}
#                 try:
#                     value = my_dict['d']
#                 except KeyError:
#                       print("Error: Key 'd' not found in dictionary")
                        
#     2.IndexError: This exception is raised when we try to access an index that is out of range for alist or other sequences.
             
#         for example:
#                       my_list = [1,2,3]
#                         try:
#                              value = my_list[3]
#                         except IndexError:
#                             print("Error : Index 3 is out of range for list")
```


```python
# 5.Explain ImportError.What is ModuleNotFoundError?
# Ans-
#     "ImportError" is a built-in Exception class in python that is raised when an imported module,package,or name cannot be found or loaded.This can occure due to various reasons such as misspelled module name,missing dependencies or incorrect python path settings.
#     for example- "ModuleNotFoundFrror" is a more specific type of "ImportError" that was introduced in python 3.6.
    
#     #python 3.6 and later
#     import foo #raises ModuleNotFoundError: No module named 'foo'
    
#     #python 3.5 and earlier
#     import foo #raises ImportError: No module named 'foo'
    
#     "ModuleNotFoundError" some other types of "ImportError"that we may encounter include:
        
#         1."ImportError:cannot import name"
#         2."ImportError:DLL load failed"
```


```python
# 6.List down some best practices for exception handling in python.
# Ans-
#       1.Catch Specific exceptions
#       2.Use try-except blocks
#       3.Use finally block
#       4.Raise exception
#       5.provide useful error messages
#       6.Log the exceptions
#       7.Use context managers
#       8.Test exception handling
```
