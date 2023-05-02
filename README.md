Download Link: https://assignmentchef.com/product/solved-cpe212-project05
<br>
<strong> </strong>




<strong><u>&lt;Project05 Directions for Executing the Sample Solution&gt;</u></strong>

You may run the sample solution by typing the following at a terminal window command prompt<strong>:  </strong>

<h1>/home/work/cpe212/project05/p05    inputfile  Note:  inputfile is called a Command-Line Argument</h1>

<strong>inputfile</strong><strong>  must be the name of a text file in your current working directory </strong><strong>All output is written to the standard output device (monitor). </strong><strong>The grade preview script for Project05 is available at </strong>

<strong>/home/work/cpe212data/project05/preview05.bash </strong>

<strong><u>&lt;Project05 Constraints&gt;</u></strong> <strong><em>On Project05, you may only use the following include files: </em></strong>

<strong><em> </em></strong>

<strong><em>#include &lt;iostream&gt;                                                              #include &lt;new&gt; </em></strong>

<strong><em>#include &lt;iomanip&gt;                                                               #include &lt;cstddef&gt; </em></strong>

<strong><em>#include &lt;fstream&gt;                                                                #include “heap.h” </em></strong>

<strong><em>#include &lt;string&gt;                                                                   </em></strong>

<strong><em>#include &lt;cmath&gt; </em></strong>

<strong><em>You are not allowed to utilize </em></strong><strong><em>Global Variables</em></strong><strong><em>!!   </em></strong>è<strong><em>  Recursive Function Calls </em></strong><strong><em>are permitted!! </em></strong>ç

<strong><em>Failure to follow these directions will result in zero (0) credit on this assignment. </em></strong>

<strong>Once you are satisfied with your solution, submit your program files via CANVAS</strong>.

<strong><em><u>NOTE: make sure that you do not change the order in which the information is entered.  An</u></em></strong><strong><em> <u>automatic script is used to process all lab submissions, and if the order of the input</u> <u>information is modified, the script will not work properly with your program.</u></em></strong> <strong><u>&lt;Project05 </u></strong><strong><u>heap.cpp</u></strong><strong><u> Description&gt;</u></strong>

<strong><em>Your goal is to </em></strong><strong><em>EXACTLY</em></strong><strong><em> match the output of your program to that of the sample solution.</em></strong>

<strong>‘c’ </strong>è <strong>Constructor</strong><strong> dynamically allocates a Heap object </strong>

<strong>‘+’ </strong>è <strong>Insert</strong><strong> the data value that appears after the ‘+’ onto the Heap </strong>

<strong>‘-‘  </strong>è <strong>DeleteMax</strong><strong> deletes the maximum value from the Heap </strong>

<strong>‘p’ </strong>è <strong>Print</strong><strong> writes the contents of Heap to </strong><strong>stdout</strong><strong>  </strong>

<strong>‘s’ </strong>è <strong>Size</strong><strong> returns the number of elements currently stored in the Heap object </strong>

<strong>‘e’ </strong>è <strong>MakeEmpty </strong><strong>empties the heap leaving it ready to accept new data </strong>

<strong>‘m’ </strong>è <strong>Capacity</strong><strong> returns the maximum number of elements currently allocated to the Heap object ‘d’ </strong>è <strong>Destructor</strong><strong> deallocates the Heap object </strong>

<strong> </strong>

<strong> </strong>

<h2>&lt;Project05 SmartHeap Class Description&gt;</h2>

The <strong>SmartHeap</strong> class uses a <strong><em>dynamically allocated</em></strong> one dimensional array to store heap values.  When this array is filled to capacity, the next insert causes creation of a new array with twice the capacity.  Values from the smaller array are copied from the small array into the new larger array, and then the smaller array is deallocated to prevent a memory leak.

When deleting the maximum value, the process of expanding the array is reversed.  When the amount of data stored within the smart heap array dwindles to less than half of the current array capacity, you must resize the array without losing any data or creating a memory leak.  When resizing the array, <strong>cut the capacity in half</strong>.  However, be sure that you do not to shrink the array below the <strong>minimum array size of</strong> <strong>DEFAULTSIZE</strong>.




The data type of the value stored in each node is determined by the client code <strong>main.cpp</strong>. è<strong> Inline functions are not allowed in this course and will result in no credit (0) </strong>ç

<strong>[Note: An </strong><strong>inline function</strong><strong> is a function whose definition appears within the class declaration] </strong>

The <strong>SmartHeap</strong> class contains three <strong>private</strong> attributes, six <strong>private</strong> functions, and eight <strong>public</strong> member functions

è <strong>See the file</strong> <strong>smartheap.h</strong> <strong>for additional details regarding the function interfaces</strong> ç

<strong> </strong>

<h2>&lt;Project05 Hints&gt;</h2>

Sample codes for the array implementation of the Heap container appear in Chapter 9 of the official course textbook,

<strong><em>C++ Plus Data Structures, Sixth edition  </em></strong>by Nell Dale, Chip Weems, and Tim Richards