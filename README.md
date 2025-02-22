**File_Handling in Python**

    File handling in Python allows you to create, read, write, and delete files easily. 
    Python provides built-in functions to work with files efficiently.
    
 **1.Opening a File**
 
     Before working with a file, we need to open it using the open() function.
     Syntax: open("file_name","mode")
     Example :file = open("example.txt", "r")         # Opens the file in read mode

  **2.Reading from a File**
  
      We can read a file using different methods:

     >>  To read the whole file
         file = open("example.txt", "r")
         content = file.read()                        # Reads the whole file
         print(content)
         file.close()  
         
     >>  To read line by line:
        file = open("example.txt", "r")
        content = file.readlines()                       
        for i in content:
            print(i.strip())
        file.close() 
        
**3.Writing to a File**

     If we want to write data to a file we need to open the file in write.Write mode creates a new file if the file 
     doesn’t exist, overwrites if file exist.

     Syntax: open("file_name","mode")
     Example :file = open("example.txt", "w")         # Opens the file in write mode
              file.write("Hello")                     # This overwrites the existing content in the file to Hello.
              file.close()                           
              
              
    >>To add content without deleting existing data, use append mode ("a"):
      file = open("example.txt", "a")
      file.write("Appending new data!\n")
      file.close()

      
**4.With Open**

     A better way to handle files is by using with, so we don’t have to worry about closing the file manually.
     
     with open("example.txt", "r") as file:
        content = file.read()
        print(content)                               # No need for file.close()



**Exception Handling in Python**
    
    Exception handling helps us deal with errors in Python without stopping the program. We use try, except, else, 
    and finally to handle errors safely.

  **1.Try-Except**
  
    In Python, we use try and except to handle errors so the program doesn’t crash.
    Syntax:
    
    try:
        # Code that might cause an error
    except ExceptionType:
        # Code that runs if an error occurs

  **2.Using else with try-except**
  
    The else block runs only if no error occurs.
    Syntax:
    
    try:
        # Code that might cause an error
        
    except ErrorType:
        # Handle the error
    else:
        # Runs only if no error occurs

  **3.Finally**
  
     The finally block always runs, whether an error occurs or not.

  Syntax:
  
    try:
        # Code that may cause an error
        
    except ErrorType:
        # Handle the error
    finally:
        # Runs no matter error occurs or not
