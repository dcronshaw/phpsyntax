# PHP syntax guide.

## PHP Comments

  ### Single Line Comments
  
Single line comments can be used to make small comments or comment out lines of code. They are created by putting `//` in       front of whatever you are commenting out. 
          
    //This is a comment in PHP 
  
  ### Multi Line Comments
  
Multi line comments are used to make larger paragraph sized comments, or to comment out mulitple lines of code. Create multi line comments by using `/*` in front and `*/` at the end.

    /* In order to comment out large blocks of code, or to create large comments, use multi line PHP comments */
    

##  Variables

 PHP variables are created by using `$` and then given a name and a  value. Values can be strings or numbers. They must also be called with `$`. PHP variable names are case sensitive. `$bear` and `$BEAR` are different variables, with potentially different values.
 
     $bear = "I am a bear."; $BEAR = 45;
     
## Echo and Print  

 Echo and Print essentially do the same thing, where they write to the DOM using parameters(HTML mark up, strings, variables, integers.). Echo can be used with multiple parameters(seperated by commas), where print can only use one. Strings and integers are surrounded by `" "` where variables are not. Strings and variables can be put together by using `.`.   
    
     $bear = "I am a bear."
 
     print "hello there.";
     
     echo "hey." . $bear;

## Data Types

  PHP supports 8 different data types. String, Integer, Float, Boolean, Object, Array, Null, and Resource.
  
  ### String
   Strings are a sequence of characters wrapped by single or double quotes.
        
          "this is an example of a string."; 'so is this.';
   
  ### Integer
   An integer is a non-decimal number between -2,147,483,648 and 2,147,483,647.
      
          2, 45, 3329932, 1111111, and -81 are all examples of integers.
          
  ### Float
   A float is a number with a decimal, or a number in exponential form.
      
         1.452, 3324.65, and 543.23 are floats.
         
  ### Booleans
   A boolean is a true/false variable. These are not case sensitive.
   
        $x=true $y=FALSE
        
  ### Arrays
   An array is a variable that holds multiple values. An array is called with array().
      
       $colours = array("red", "blue", "green", "purple");
  
  ### Objects
   An object is similar to an array, kind of like an array of arrays. Objects are sperated by classes,(cars, fruits, books, etc.) then each class can create new objects.
   
   
        class Books {
       // Members of class Books
        }

        // Creating three objects of Books
        $physics = new Books; 
        $math = new Books;
        $chemistry = new Books;
        
   Objects can then be assigned new properties and values.
   
      $physics->setTitle( "Physics for High School" );
      $chemistry->setTitle( "Advanced Chemistry" );
      $math->setTitle( "Algebra" );
      
   Then properties of the object can be called.
   
      $math->getTitle();


   ### Null
   
   Something that doesn't have a value is considered null. Note: 0 is not null. Null is the absence of a value.
   
        $a = NULL;
        
   ### Resource
   
   A resource is a variable that holds resources to an outside source. It is used to access a database or similar resources.
   
        $results = mysqli_query($db, "SELECT * FROM info");
        
        
 ## Constants
 
  A constant is a name of a simple value, and this value cannot be changed as long as the script exists. To create a constant, use define().
  
      define(name, value, case-insensitive)
      
 A constant takes 3 parameters, name, value, and case-insensitive(case-sensitivity is false by default.)
 
 ## Operators
 
  Operators are used to perform operations on variables and values.

Following are the various groups of operators.

    Arithmetic operators
    Assignment operators
    Comparison operators
    Increment/Decrement operators
    Logical operators
    String operators
    Array operators
    Conditional assignment operators
    
    
Some useful operators include:

      == Equal     
      === Identical 
      !== not equal
      !=== not identical
      < Lesser than
      > Greater than
      =< Equal to or less than
      => equal to or greater than
      ++$x pre-increment
      $x++ post-increment
      --$x pre-decrement
      $x-- post-decrement
      + addition
      - subtraction
      * multiplication
      / division
      
      more operators can be found: `https://www.w3schools.com/php/php_operators.asp`
      
  ## If, else, elseif
  
   Sometimes we need conditions to control when our functions take effect. 
   
   
   ### If
   
   If statements give a requirement for a function to run.
   
      if(condition_exists){
        do this 
        
      }
      
   ### Else
   
   Else statements take effect if the if statement is false.
   
      if(condition_exists){
        do this
        
       }
       else{
       
       do this other thing
       
      }
      
   ### Elseif
   
   Elseif statements take effect if the if statement is false, but the elseif is true.
   
      
      if(condition_exists){
        do this
        
       }
       elseif{
       
       do this other thing
       
      }
      else{
      
      do the third thing
      
      }
      
  ### Functions
  
   Functions are created to perform certain tasks. Functons are created using `function`.
   
      function doathing(){
      
            do this thing;
            
       }
       
   Functions can be created to accept arguments as well.
   
      function addthesenumbers($x, $y){
      
          echo($x + $y);
          
     }
     
   Functions can then be called by using their name such as `doathing()`
   
      
       addthesenumbers(4, 7);
       
  
  
  ### Loops
  
   Loops allow for the same function to perform as long as certain conditions are true.
   Loops have the following types:
   
      while - loops through a block of code as long as the specified condition is true
      do...while - loops through a block of code once, and then repeats the loop as long as the specified condition is true
      for - loops through a block of code a specified number of times
      foreach - loops through a block of code for each element in an array
      
   ## While
   
      while(this thing is true){
      
          do this;
       }
       
   ## Do...while
   
      do{
        this;
       }while(this thing is true);
       
   ## For
   
      $x = 0;
      
      for($x = 0; $x<=15; $x++;){
        
        echo $x;
        
      }
      
   ## Foreach
   
      $cars = array("BMW", "Volvo", "Lincoln");
      
      foreach($cars as $value){
       echo $value "<br>";
       
      }
