Download Link: https://assignmentchef.com/product/solved-cs-202-computer-science-ii-project-3
<br>



<strong> </strong>

<strong>  </strong>




<strong>Objectives:  </strong>The two main objectives of this project is to test your ability to (1) create and use pointers, and (2) create and use C++ classes. A review of your knowledge of structs, arrays, iostream, file I/O and C-style strings is also included.

<strong>Description: </strong>

This project will expand Project 2 by adding additional functionality, using pointers, and implementing abstract data types (ADTs) through classes. <strong>Pointers must be used for all array manipulation</strong>, including arrays with ADTs (structs, classes) e.g, rental cars, rental agencies. <strong>Pointers must be used in function prototypes and function parameter lists</strong> – not square brackets. Make sure <u>all your C-string functions</u> (e.g. string copy, string compare, etc.) work with pointers (parameters list and function implementation). <u>Square brackets</u> are to be used <u>only when declaring an array</u>. <strong>For this project, pointers can only be moved by conducting post/preincrement/decrement operations on them </strong>(i.e., ++ or – -), or by <strong>setting the pointer back to the base address</strong> using the array name. All pointers must be passed by value. (<u>Note:</u> Try to use the arrow operator (-&gt;) with Class Object pointers for member access, if you use such in your code.)




The new functionality is as follows: You are given an updated data file (e.g. Agencies.txt) where there are 3 rental Car Agency locations, where <strong>each of the 3</strong> locations (<strong>RentalAgency</strong>) has <strong>5</strong> cars (<strong>RentalCar</strong>). You will have <strong>similar menu options</strong>, but the <strong>functionality has been updated</strong> below. Note: using multiple helper functions to do smaller tasks will make this project significantly easier. You may want to create a function that will get a car from a location based on the location and car indices.




<strong>The RentalCar Class will contain the following data members: </strong>

<ul>

 <li><strong>m_year</strong>, an int (year of production)</li>

 <li><strong>m_make</strong>, a C-string (char array of 255 maximum size)</li>

 <li><strong>m_model</strong>, a C-string (char array of 255 maximum size)</li>

 <li><strong>m_price</strong>, a float (price per day)</li>

 <li><strong>m_available</strong>, a bool (1 = true; 0 = false; try to display true/false using the</li>

</ul>

“std::boolalpha” manipulator like: cout &lt;&lt; boolalpha &lt;&lt; boolVariable; ) <strong>and will have the following methods: </strong>

<ul>

 <li><strong>Default Constructor</strong> – will set the aforementioned data members to default initial values (<em>Hint</em>: Remember to use properly named constants where appropriate).</li>

 <li><strong>Parameterized Constructor</strong> – will create a new object based on the values passed into it (All the above values are expected to be present in the function parameters list, and all should be used to initialize the instantiated Object member variables).</li>

 <li><strong>Separate Get and Set methods </strong>for all data members.</li>

 <li><strong>Print </strong>– will print out all the car’s data.</li>

 <li><strong>EstimateCost</strong> – will estimate the car’s cost <em>given</em> (via a parameter passed to it) a number of days to rent it for.</li>

</ul>




<strong>The RentalAgency ADT will be a struct and will contain the following data members: </strong>

<ul>

 <li><strong>name</strong>, a C-string (char array of 255 maximum size)</li>

 <li><strong>zipcode</strong>, an int array of size 5 (<em>Hint</em>: You will <em>NOT</em> be able to use cin and cout –or any fstream objects– directly with this int array as you were doing so far with C-strings. The reason is that reading/writing is specially handled by C++ for char array types. You will need to manage reading/writing to an int array on your own.)</li>

 <li><strong>inventory</strong>, an array of RentalCar objects with a size of 5</li>

</ul>




<strong>The menu must have the following entries, each implementing a functionality: </strong>

<strong>1) Ask</strong> the user for the<strong> input file name</strong>, and then <strong>read ALL</strong> data from that <strong>file</strong>. Then, <strong>read ALL</strong> data from that <strong>file</strong> (the file has been <strong>structured</strong> where the <u>first line is the Car Agency</u> info, <u>followed by 5 cars</u>). The data have to be stored into <strong>arrays of Class Objects</strong>.

<ul>

 <li><strong>2) Print out to terminal ALL</strong> data for <strong>all Agencies</strong> and <strong>all their corresponding Cars</strong> in a way that demonstrates this relationship (see Sample Output section).</li>

 <li><strong>3) Estimate</strong> car <strong>rental cost</strong> – <strong>prompt</strong> for: a) an <strong>Agency</strong> (e.g., Hertz – <u>you can do so with a </u></li>

</ul>

<u>1-3 </u><u>int number per-Agency</u>), and b) a <strong>Car number</strong> (<u>where 1-5 are the cars at each agency</u>).

<ul>

 <li><strong>4) Find</strong> the <strong>most expensive</strong> Car – <strong>Print to terminal</strong> the single most expensive Car out of all 3 Agencies.</li>

 <li><strong>5) Print out </strong>only the <strong>available</strong> <strong>Cars</strong> – from <strong>all Agencies</strong>, to a <strong>separate output file</strong> (when the user chooses menu entry 5, they should also get <strong>asked</strong> for an <strong>output file name</strong>).</li>

 <li><strong>6) Exit</strong></li>

</ul>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>The following minimum functionality and structure is required: </strong>

<ul>

 <li>Ask the <strong>user</strong> for the <strong>input file </strong></li>

 <li>The list(s) of cars must be stored into <strong>array(s) of Class Objects</strong>.</li>

 <li>Use <strong>character arrays</strong> to hold your strings (i.e., C-style) exclusively (using the string data type is still not allowed).</li>

 <li>Write <strong>multiple functions</strong> (Hint: each menu option should be a function).</li>

 <li>At least on function must use <strong>pass by-Reference</strong>. Otherwise, as before, you are free to use <strong>pass by-Value, pass by-Reference</strong>, <strong>pass by-Address</strong> for your function parameters. (<em>Note</em>: Remember that using pass by-Value will make the function work on a local internal copy of whatever variable you pass as an argument, therefore the change will not be made on the actual argument itself, and it will be left unaffected after the function call is complete).</li>

 <li><strong>Pointers </strong>must be used for<strong> all array manipulation</strong> (iterating over elements to read/modify <u>cannot</u> be performed with bracket operator accessing).</li>

 <li><strong>Pointers </strong>must be used in<strong> function prototypes </strong>and<strong> function parameter lists </strong>(the bracket notation is not allowed in parameters lists).</li>

 <li><strong>Pointers </strong>can only be<strong> moved by incrementing or decrementing</strong>:</li>

</ul>

<h1>double d[3] = {1,2,3}; double* d_Pt = d;</h1>

<strong>for</strong><strong> (</strong><strong>int</strong><strong> i=0; i&lt;3; ++i,++d_Pt){ </strong><strong>cout</strong><strong> &lt;&lt; </strong><strong>*</strong><strong>d_Ptd; } </strong>Ø Or by<strong> setting </strong>the pointer<strong> back to the base address</strong> using the array name.

<h1>d_Pt = d;  cout &lt;&lt; *d_Pt &lt;&lt; endl;</h1>

Ø Write your <strong>own C-string copy</strong>, <strong>C-string compare</strong> functions. Their prototypes will have the form (you must use the prototypes exactly as provided, with <strong>char *</strong> parameters):

<strong>// copies characters from source to destination until a NULLcharacter ‘ ’ is found in source, then it NULL-terminates destination too, and returns  </strong><strong>void</strong> <strong>myStringCopy</strong><strong>(</strong><strong>char *</strong><strong> destination, </strong><strong>const char * </strong><strong>source);</strong>

<strong> </strong>

<strong>// returns 0 when the strings match, i.e. their characters are equal one-by-one until a NULL-character ‘ ’ is found in both strings and at the same position as well </strong>

<strong>// returns a value &lt;1 if the first character that does not match has a lower value in str1 than in str2 </strong>

<strong>// returns a value &gt;1 if the first character that does not match has a higher value in str1 than in str2  </strong><strong>int </strong><strong>myStringCompare</strong><strong>(</strong><strong>const char *</strong><strong> str1, </strong><strong>const char *</strong><strong> str2); </strong>

<sup>  </sup>Ø The other functionality and structure of the program should remain the <strong>same as Project #2</strong>, including <strong>writing to screen</strong> and <strong>file</strong>, as well as<strong> restrictions on string</strong> libraries, <strong>global variables</strong> and <strong>constants</strong>, etc.




<strong>Implement the concepts of encapsulation and data hiding as much as possible! </strong>

<strong>            </strong>This is a chance to experiment as much as possible with classes, and their concepts as taught in class. It is not a strict requirement that all RentalCar data members are private at this point. Try your best in order to acquaint yourself with these new concepts at this early point, so that it pays off in future project which will impose such hard requirements.







<strong>Sample Output for menu option 2: </strong>




Hertz 93619

2014 Toyota Tacoma , $115.12 per day , Available: true

2012 Honda CRV , $85.1 per day , Available: false

2015 Ford Fusion , $90.89 per day , Available: false

2013 GMC Yukon , $110.43 per day , Available: false

2009 Dodge Neon , $45.25 per day , Available: true

Alamo 89502

<ul>

 <li>Toyota Rav4 , $65.02 per day , Available: true</li>

 <li>Mazda CX5 , $86.75 per day , Available: true</li>

</ul>

2016 Subaru Outback , $71.27 per day , Available: false

2015 Ford F150 , $112.83 per day , Available: true

2010 Toyota Corolla , $50.36 per day , Available: true

Budget 93035

<ul>

 <li>Ford Fiesta , $42.48 per day , Available: false</li>

 <li>Dodge Charger , $55.36 per day , Available: true</li>

</ul>

2012 Chevy Volt , $89.03 per day , Available: false

2007 Subaru Legacy , $59.19 per day , Available: false

2010 Nissan Maxima , $51.68 per day , Available: true <strong> </strong>

<strong>The completed project should have the following properties: </strong> Ø Written, compiled and tested using Linux.

<ul>

 <li>It must compile successfully using the g++ compiler on department machines. Instructions how to remotely connect to department machines are included in the Projects folder in WebCampus.</li>

 <li>The code must be commented and indented properly.</li>

</ul>

Header comments are required on all files and recommended for the rest of the program. Descriptions of functions commented properly.

<ul>

 <li>A one page (minimum) typed sheet documenting your code. This should include the overall purpose of the program, your design, problems (if any), and any changes you would make given more time.</li>

</ul>

<strong> </strong>

<strong>Turn in:</strong> Compressed .cpp file and project documentation.























