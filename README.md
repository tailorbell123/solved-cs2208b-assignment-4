Download Link: https://assignmentchef.com/product/solved-cs2208b-assignment-4
<br>
<h1>Strings</h1>

A string is an array representing a sequence of characters. To store a string of <em>n</em> characters in your program, you need to set aside <em>n+1</em> bytes of memory. This area of memory will contain the characters in the string, plus one extra special character—the <em>null</em> character—to mark the end of the string. The <em>null</em> character is a byte whose bits are all zeros (0x00). The actual string consists of any group of characters, which none of them can be the <em>null</em> character.




<h2>QUESTION 1 (25 marks)</h2>

Draw <u>a <em>detailed flowchart</em></u> and write an ARM assembly language <em><u>program</u></em> to concatenate two stings (<strong>STRING1</strong> and <strong>STRING2</strong>) and store the result in a <em>null</em> terminated <strong>STRING3</strong><strong>. </strong>Assume that the length of <strong>STRING1</strong> + the length of

<strong>STRING2</strong> ≤ 255.

<strong><em>Your code should be highly optimized, i.e., use as little number of instructions as possible.</em></strong>

You may want to define the strings as follow:

<strong>STRING1 DCB “This is a test string1”   ;String1 </strong>

<strong>EoS1    DCB 0x00                       ;end of string1 </strong>

<strong>STRING2 DCB “This is a test string2”   ;String  </strong>

<strong>EoS2    DCB 0x00                       ;end of string2 STRING3 space 0xFF </strong>

<strong> </strong>

<h2>QUESTION 2 (35 marks)</h2>

Draw a <em><u>detailed flowchart</u></em> and write an ARM assembly language <em><u>program</u></em> to copy a <em>null</em> terminated <strong>STRING1</strong> to a <em>null</em> terminated <strong>STRING2</strong>, <u>after removing any occurrences</u> of the word “<strong><em>the</em></strong>” in <strong>STRING1</strong>. I.e., if <strong>STRING1</strong> is  “<strong>the</strong> woman and <strong>The</strong> man said <strong>the</strong>” then <strong>STRING2</strong> would become “ woman and <strong>The</strong> man said ”. However, if <strong>STRING1</strong> is “and <strong>the</strong>y took brea<strong>the</strong>” then <strong>STRING2</strong> would become

“and <strong>the</strong>y took brea<strong>the</strong>” without any change.

<strong><em>Your code should be highly optimized, i.e., use as little number of instructions as possible.</em></strong>

You may want to define the strings as follow:

<strong>STRING1 DCB “and the man said they must go”   ;String1 </strong>

<strong>EoS     DCB 0x00                              ;end of string1 STRING2 space 0xFF </strong>

<strong> </strong>

<h2>QUESTION 3 (40 marks)</h2>

Draw a <em><u>detailed flowchart</u></em> and write an ARM assembly language function (subroutine) that takes a data value stored in register <strong>r0</strong> and returns a value in <strong>r0</strong> as well. The function returns <em>y = a × x<sup>2</sup></em> <em>+ b × x + c </em>where <em>a</em>, <em>b</em>, and <em>c</em> are signed integer parameters built into the function (i.e., they are not passed to it) and are defined in the memory using three <strong>DCD</strong> instructions. The subroutine also performs clipping, i.e., if the output is greater than a value <em>d</em>, it is clipped to <em>d</em>, where <em>d</em> is another parameter defined in the memory using a <strong>DCD</strong> instruction. The input in <strong>r0</strong> is a signed integer binary value. Apart from<strong> r0</strong>, <u>no other registers may be modified by this subroutine</u>, i.e., if you want to use any register as a working register, you have to store its value in a safe place first prior changing it, and to restore this value before returning from the function.

After implementing the function, write an assembly program which stores a value in <strong>r0</strong> and calls your function. Once the control is returned back from the function, the program will double the returned value and store this doubled value in <strong>r1</strong>.  <strong><em>Your code should be highly optimized, i.e., use as little number of instructions as possible.</em></strong><em> <strong>Example1</strong></em>: if <em>a = 5, b = 6, c = 7, d = 90</em>, and <strong>r0</strong><em> = 3</em>,                     then the returned value in <strong>r0</strong> should be 70 and the value in <strong>r1</strong> will be 140. <strong><em>Example2</em></strong>: if <em>a = 5, b = 6, c = 7, d = 50</em>, and <strong>r0</strong><em> = 3</em>,                     then the returned value in <strong>r0</strong> should be 50 and the value in <strong>r1</strong> will be 100. <strong><em>Example3</em></strong>: if <em>a = -5, b = 6, c = 7, d = 10</em>, and <strong>r0</strong><em> = 3</em>,                     then the returned value in <strong>r0</strong> should be -20 and the value in <strong>r1</strong> will be -40.

Copyright © 2016 Mahmoud El-Sakka.


