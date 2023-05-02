Download Link: https://assignmentchef.com/product/solved-comp135-assignment-1
<br>
This assignment will get you started using NumPy. If you are new to using that library (or Python in general), you probably want to start with the tutorial provided at:

<a href="https://numpy.org/devdocs/user/quickstart.html">https://numpy.org/devdocs/user/quickstart.html</a>

You have been supplied with some starter code, including the prototype for two functions that you need to complete. The code also contains detailed documentation of how the functions should operate, and some examples of their use. You can (and should) test your code to confirm that it does what is asked.

<ol>

 <li>Along with your code, submit a completed version of the txt file.</li>

</ol>

An example has been provided, which you should edit appropriately to include:

<ul>

 <li>Your name.</li>

 <li>The time it took you to compete the assignment.</li>

 <li>Any resources you used to complete the assignment, including discussions with the instructor, TA’s, or fellow students, and any online or offline resources consulted. If you did not need to consult any outside resources, you can say so.</li>

 <li>A brief description of what parts, if any, of the assignment caused you to seek help.</li>

</ul>

<ol start="2">

 <li>The first part of the code asks you to write a function to split data into a training set and a testing set (a very common task in ML). Your code will use basic NumPy array indexing and random number generation to take an input array containing <em>L </em>instances of <em>F</em>-dimensional data, and divide it into two mutually exclusive arrays of size <em>M </em>(for training) and <em>N </em>(for testing).</li>

</ol>

As part of its input, the function takes parameter frac_test, specifying the overall fraction of the data-set to use for testing purposes. It will use this fraction to determine the size <em>N</em>, <strong>rounding up </strong>to the nearest whole number: <em>N </em>= dfrac_test∗ <em>L</em>e

The function will also use NumPy functions like shuffle or permutation for doing random sampling of the data, so that the test/train instances are uniformly selected from the data-set:

(Note that this links to a library that has been generally replaced by something a bit newer in the latest version of NumPy, but is still supported. Your code will function correctly if you use the legacy version, or the newer NumPy features.) Furthermore, we want the results of the function to be <em>reproducible</em>, for scientific purposes. That means that there should be a way to specify a source of randomness (a <em>seed</em>) such that it is possible to duplicate any random selection. In NumPy, this is generally handled by using a RandomState instance, or via an integer seed. See the linked discussion from the source code comments for insight into using such seeds in your code.

<strong>Notes</strong>: read the documentation of the function supplied with the starter code carefully. Ensure that your code meets the requirements as given. In addition, be sure that your code uses <em>only </em>basic Python and functions from NumPy. <em>Do not </em>call functions for data-set generation and manipulation from libraries like sklearn.

<ol start="3">

 <li>The other function you are to complete finds <em>nearest neighbors </em>of given datainstances. That is, given a set of <em>F</em>-dimensional data of size <em>N</em>, and <em>Q </em>query instances (also <em>F</em>-dimensional), we want to compute the <em>K </em>closest vectors found in the data, for some integer value <em>K</em>, and for each query instance (for a total of <em>Q </em>× <em>K </em>neighbors).</li>

</ol>

In computing “closeness,” we will use the <em>Euclidean distance </em>between vectors. For two vectors

<ol>

 <li><strong>x</strong>) and <strong>x</strong>), this distance is given by:</li>

</ol>

Your function will take in a data-set (a 2-dimensional array of size <em>N </em>× <em>F</em>) and a query-set (a 2-dimensional array of size <em>Q</em>×<em>F</em>), and return a 3-dimensional array (of size <em>Q</em>×<em>K </em>×<em>F</em>), where each row (indexed by <em>Q</em>) consists of the <em>K </em>nearest neighbors of the corresponding query vector. These neighbors should appear <em>in order</em>, closest to least-close.

<strong>Notes</strong>: it is possible that there will be ties among neighbors. If this occurs, such ties can be broken however you like (randomly or not). Again, be sure that your code uses <em>only </em>basic Python and functions from NumPy. <em>Do not </em>call functions from libraries like sklearn.