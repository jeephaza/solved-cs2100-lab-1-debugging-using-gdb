Download Link: https://assignmentchef.com/product/solved-cs2100-lab-1-debugging-using-gdb
<br>
<strong>GNU Debugger (GDB)</strong> <a href="https://www.gnu.org/software/gdb/">/</a>

A debugger is used to analyze program execution in a step-by-step and detailed manner. It is used to find bugs in a program. Using a debugger, we can execute a program partially and view the status of the variables and resources being used the program to identify any discrepancies. <strong>GDB </strong>is an open source, freely available debugger which can be used for multiple languages.

GDB can do four main kinds of things (plus other things in support of these) to help you catch bugs in the act:

<ul>

 <li>Start your program, specifying anything that might affect its behaviour.</li>

 <li>Make your program stop on specified conditions.</li>

 <li>Examine what has happened, when your program has stopped.</li>

 <li>Change things in your program; so that you can experiment with correcting the effects of one bug and go on to learn about another.</li>

</ul>




<h1>GNU Compiler Collection (GCC)</h1>

GCC is an open source compiler system used to compile C/C++ programs: <a href="https://gcc.gnu.org/">https://gcc.gnu.org/</a>

<strong> </strong>

<strong>Objective:</strong>

You will learn how to use <strong>GDB </strong>to debug a C program.




<strong>Preparation (before the lab): </strong>

<ol>

 <li>Install GDB:

  <ol>

   <li><strong>Ubuntu: </strong>sudo apt-get install gdb</li>

   <li><strong>OSX: </strong>brew install gdb</li>

   <li><strong>Windows: </strong>

    <ul>

     <li>Download Cygwin (<a href="https://cygwin.com/install.html">https://cygwin.com/install.html</a><a href="https://cygwin.com/install.html">)</a></li>

    </ul></li>

  </ol></li>

</ol>

<strong> </strong>

<ul>

 <li>Select <strong>develop</strong> packages during installation:</li>

</ul>

<strong> </strong>

<strong> </strong>

<ul>

 <li>Start Cygwin terminal from the start menu:</li>

</ul>










<ol start="2">

 <li>Starting GDB (all platforms): Type GDB in the terminal (Cygwin terminal for windows users). <strong>Help </strong>command lists the help and <strong>quit </strong>command exits GDB.</li>

</ol>

<strong> </strong>

<strong> </strong>

<strong>Procedure</strong>:

<ol>

 <li>The cs2100lab1.zip file contains a file called <strong>c</strong>, which you will require.</li>

</ol>




<ol start="2">

 <li>Compile <strong>c</strong> with <strong>gcc </strong>using the following command: <strong>gcc –g –o lab1 lab1.c</strong></li>

</ol>




<ol start="3">

 <li>What is the purpose of the flags “g” and “o” in gcc?</li>

 <li>Execute the program you just compiled using the command: <strong>./lab1 </strong>(for windows type:</li>

</ol>

<strong>lab1</strong>). What is the error encountered (if any!)?




Answer: ______________________________________________________




<ol start="5">

 <li>Start the GDB debugger by using the command: <strong>gdb lab1</strong></li>

</ol>




<ol start="6">

 <li>To run the program in GDB, you can use the command This will run the whole program without any pause. Type <strong>run </strong>to execute the program.</li>

</ol>




<ol start="7">

 <li>To get into the debug mode use the <strong>start</strong> command</li>

</ol>




<ul>

 <li>You can use the <strong>list</strong> command to view the source code at any point</li>

 <li>You can also use <strong>layout src </strong>and <strong>layout asm </strong>commands to view source code and assembly code in a split screen.</li>

</ul>




<ol start="8">

 <li>A <strong>breakpoint </strong>is a command to put an intentional pause in the program execution to inspect the variable values and resources in the program. You can set multiple breakpoints in a program. In GDB you can put a breakpoint at any line number using the command:</li>

</ol>




<h1>&gt; break lineNumber or &gt; b lineNumber<em>  </em></h1>




Example: This will put a breakpoint on line 6<strong> &gt; break 6 </strong>




Now if you run the program, <strong>it will pause at line 6. </strong>You can continue execution (till end or the next breakpoint) using the <strong>continue </strong>command.




Which line(s) will you set the breakpoint(s) in?




Answer: ___________________________________________________________




<ol start="9">

 <li>A <strong>step </strong>command is used to carry out step-by-step execution of the program. You can <em>step </em>through the program using the following command:</li>

</ol>




<h1>&gt; step</h1>

This will execute only the next line of code or

<h1>&gt; step numberOfLines</h1>




E.g. <strong>&gt; step 3</strong> will execute next three lines of code




<ul>

 <li>You can “switch on” display of the associated assembly code <sub>      </sub>related to the instruction being executed using the command:  <strong>set disassemble-next-line on</strong></li>

</ul>




<ol start="10">

 <li>At every step (or breakpoint) you can view a variable value using the <strong>print </strong>command:</li>

</ol>

<strong>&gt; print a </strong>




You can view all local variable values using the command:

<h1>&gt; info locals</h1>




What are the values of variables <strong>c </strong>and<strong> d at the start of line 8 </strong>(<em>before executing line 8</em>)<strong>? </strong>







Answers: _______________________________________________________________




<ol start="11">

 <li>You can view the register values at any step or breakpoint using this command:</li>

</ol>




<h1>&gt; info registers</h1>




<ol start="12">

 <li>You can stop the debugging by using the <strong>stop</strong> To quit GDB, use the <strong>quit</strong> command.</li>

</ol>




<ol start="13">

 <li>Debug and modify <strong>c </strong>to carry out four arithmetic operations (+, -, /, *) and print the days of the week. The output of the program should look as follows:</li>

</ol>




<ol start="14">

 <li></li>

</ol>