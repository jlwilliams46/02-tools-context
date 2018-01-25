1. When this code is run in Node, e.g. node index.js, what are the two stages of execution for this file called, and which order do they happen in?

    The two stages of execution for this file are called Compilation and Execution. The Compilation Stage happens first. Then the Execution stage happens second.

2. Write an explanation, using as much space as you need, relating to how the first stage of execution for this file operates.

   - For example, identify the high level steps in a line by line overview and then define what each of those steps are accomplishing.

    * In Line 1: Strict Mode, a feature of ECMAScript 5, is utilized to catch common coding errors and for ensuring best practices are followed. Declaring it at the beginning of any file or function to enable strict mode.
    * In Line 3, a variable named foo is declared..
    * In Line 5, function bar is declared, its scope is global.
    * In Line 8, function baz is declared inside the scope of the bar function with a argument of foo.
    * In Line 11: a variable named bam is initialized inside the function of baz.

3. Write an explanation, using as much space as you need, relating to how the second stage of execution for this file operates.

    * In Line 3, a variable named foo is declared.
    * In Line 6, a variable named foo is initialized inside the bar function scope.
    * In Line 8, function baz is declared inside the scope of the bar function with a parameter of foo.
    * In Line 10: a variable named foo is initialized inside the function of baz.
    * In Line 11: a variable named bam is initialized inside the function of baz.
    * In Line 13: baz function is called.

4. During the second stage of execution how many scopes have been registered by the engine?

    - Which segments of the code do they belong to?
    - Please identify any variables/refs and which scope each belongs to?

    * During the second stage of execution, foo had global scope and function scope, bar has global and function scope, and bam had global and function scope. 


5. When line 13 invokes the baz function, which foo will be assigned a value of bam? More specifically, bam will be assigned to the foo in ??? scope. Give a brief description in your own words to support your conclusion.

    * Since variable baz and foo are inside the function of baz, the baz function scope of foo will be assigned to bam. This is because the foo being referenced inside the baz function only exists there. 

6. Which scope, if any, will the variable bam on line 11 be registered to when the first stage of execution occurs on this file? Provide a brief description in your own words to support your conclusion.

    * Line 11 is where bam throws the reference error, because its not properly scoped.


7. For each line, 16 through 19, what is the return value for each?

    * In Line 16: bar() will return undefined.
    * In Line 17: foo will return 'bar'.
    * In Line 18: bam will throw a reference error. 
    * In Line 19: wont return anything because Line 18 threw a reference error.