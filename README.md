Download Link: https://assignmentchef.com/product/solved-cop3503-lab-4-dynamic-array
<br>
<h1>Overview</h1>

In this assignment you are going to create a class called DynamicArray. The purpose of this class is to store an array that will make use of the C++ concept of templates to store any type of data. In addition, you will write functions to expand or shrink the array as needed.

<h1>Description</h1>

All programs need storage of some kind as they execute. Arrays are the most basic, and probably the most common form of storage. However, because of their fixed nature they can be problematic to use, particularly if you need to store data of varying lengths as your application’s needs change over time. One of the first data structures people start to use in any programming language is some form of an expandable array. Java has the ArrayList class, C# has the List class, and even C++ has the vector&lt;T&gt; class.

The DynamicArray class you create will be very similar to the vector&lt;T&gt; class. The concepts behind allocating and freeing memory will be applicable when implementing numerous other data structures and algorithms, so you aren’t reinventing the wheel here. You’re learning how wheels are made, so you can build your own, custom version of them as needed in later projects.

<h1>Templates</h1>

Templates in C++ can be a bit confusing at first, but they allow you to reuse code very easily. By defining a class as a template, you can create multiple instances of that class to use different types. For example:

Foo&lt;int&gt; a; // Instance of Foo which uses ints

Foo&lt;float&gt; b; // Instance of Foo which uses floats

Foo&lt;Bar&gt; c; // Instance of Foo which uses Bars

The DynamicArray class you write is going to be a storage container, and while you may create storage containers in the future that are custom-built to solve a single problem, reusable code can make your life much easier.

<h1>DynamicArray</h1>

<h2>Storage</h2>

Internally, a class like this does not store much data. There are only three data members that you are required to store (though you may add any additional variables you see fit to help you write this).

<ul>

 <li>Data – A pointer to the data you are storing. This will be based on the <strong><em>type-id</em></strong> you define for the template. This pointer is the core of this class. It’s where the magic happens.</li>

 <li>Size – How many objects are being stored currently?</li>

 <li>Capacity – How many objects COULD be stored? This is not the same as the size. Think of a 2-car garage. Its capacity is 2, but at any given point it may have 0, 1, or 2 cars parked in it.</li>

</ul>

<h2>Functions</h2>

A class like this is all about its functionality. Basic arrays do absolutely nothing. A class like this becomes much more useful when it can DO something. First, the basics—data access. Then, the mutators. Last, but not least, constructors and the Big Three.

Why use a function AND an overloaded operator to do the same thing? Truthfully, you don’t NEED to (in your own projects, that is—you DO need to for this assignment), but it’s good experience to see that there is more than one way to accomplish something in code.

The Resize() function should print out the old capacity, as well as the new capacity. You wouldn’t normally have this in the final version of a class like this, but this can be helpful to illustrate what’s happening. You can print this with a line such as this:

cout &lt;&lt; “Resizing… old capacity: ” &lt;&lt; (TheOldCapacity) &lt;&lt; ” New capacity: ” &lt;&lt; (TheNewCapacity) &lt;&lt; endl;




And of course, the Big Three, or Trilogy of Evil, whichever you prefer. Plus, a pair of constructors. They might be evil. They might not be. Hard to say. But keep an eye on them, just in case.




<strong> </strong>

<h2>Exceptions</h2>

For functions which attempt to do something with a particular index, you will want to check to see if the indicated index is in a valid range. (Arrays have a valid range from 0 to arraySize-1.) If it isn’t, you want to <strong>throw</strong> an exception–there are many ways you can handle exceptions, but in this assignment just throwing an exception of type runtime_error(“Error! Invalid Index”) will be acceptable. There is a section in your textbook which has examples of throwing and catching exceptions. You will also have to include the file &lt;stdexcept&gt;, and be sure you are using std::runtime_error.

<h3>Examples</h3>

A few examples of things you might want to do with an array:

<h1>Tips</h1>

A few tips about this assignment:

<ul>

 <li>Remember the “Big Three” or the “Rule of Three” o If you define one of the three special functions (copy constructor, assignment operator, or destructor), you should define the other two. The entire purpose of this class is based on the concept of dynamic memory allocation.</li>

 <li>Don’t try to tackle everything all at once. Work on one function at a time. Be sure one thing works before moving on—that one thing could very well break a lot of other things later!</li>

 <li>Create your own tests! While the assignment submission on zyBooks has a lot of tests you will ultimately be graded on, you can/should be writing your own code to test functionality as you go. This also helps you to better understand your own code. Plus, it’s just good practice.</li>

 <li>Refer back to the recommended chapters in your textbook as well as lecture videos for an explanation of the details of dynamic memory allocation or templates o There are a lot of things to remember with memory allocation and deallocation</li>

 <li>If you think some of these tips seem familiar, you aren’t going crazy… it’s almost as if they are applicable to lots of situations in programming…</li>

</ul>

<strong>Program output: </strong>





