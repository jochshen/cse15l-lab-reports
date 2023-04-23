# **Lab Report 2 - Servers and Bugs (Week 3)** #

**Code**
![Image](LabImages2/code.png)

First Call:
![Image](LabImages2/ex1.png)
- new ArrayList<String> s is created on line 10 with no values inside. 
- String ```result``` is empty 
- ```.getPath()``` used with ```.equals()``` with argument "/add-message" to check if the url contains the string "/add-message" in its path
- ```getQuery()``` is passed with ```.split()```. ```getQuery()``` returns a new String with all characters after the "?". From
  there, ```.split()``` is passed with "=" to create the array {"s", "10000000000000000000000000000"}.
- ```.add()``` is called to ```ArrayList``` s with argument "parameters[1]" or "10000000000000000000000000000" 
- ```ArrayList s``` now looks like {"10000000000000000000000000000"}
- a for loop concatenates all the elements of ```ArrayList s``` to ```results. 
- The 10000000000000000000000000000 is casted into a String once you type it into the URL 
- Other than that, no other values are changed. Argument ```URI url``` isn't changed because new variables are created based off the argument. 


  
  
**Second Call:**
![Image](LabImages2/ex2.png)
- ```ArrayList s``` looks like {"10000000000000000000000000000"} since it was craeted outside the method
- String ```result``` is empty because the method is called once again 
- ```.getPath()``` used with ```.equals()``` with argument "/add-message" to check if the url contains the string "/add-message" in its path
- ```getQuery()``` is passed with ```.split()```. ```getQuery()``` returns a new String with all characters after the "?". From
  there, ```.split()``` is passed with "=" to create the parameter array {"s", "bye-bye"}.
- ```.add()``` is called to ```ArrayList s``` with argument "parameters[1]" or "bye-bye" 
- ```ArrayList s``` now looks like {"10000000000000000000000000000", "bye-bye}
- a for loop concatenates all the elements of ```ArrayList s``` to ```results```. 
- No values are changed. Argument ```URI url``` isn't changed because new variables are created based off the argument. 

  
  
  
