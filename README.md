Download Link: https://assignmentchef.com/product/solved-ucs1411-exercise-11-file-allocation-techniques
<br>
To develop a C program to implement the various file allocation techniques.

Algorithm:

<ol>

 <li>Get Main memory size and block size as input.</li>

 <li>Create a Main memory with ‘n’ number of blocks of equal size.</li>

 <li>Main memory is maintained as Linked List with structure containing block id, Free / Filename,  Link  to  next  Memory  block  ,  Link  to  Next File  block  (only  for  Linked Allocation),  File  block  table(  integer  array  to  hold  block  numbers  only  for  Indexed Allocation)</li>

 <li>Get the number of files and their size as input.</li>

 <li>Calculate the no. of blocks needed for each file.</li>

 <li>Select the Allocation Algorithm.</li>

</ol>

– For every algorithm display Directory information and File information.

<ol start="7">

 <li>For Contiguous Allocation – For each file do the following

  <ol>

   <li>Generate a random number between 1 to ‘n’</li>

   <li>Check for  continuous  number  of  needed  file  free  blocks  starting  from  that  random block no.  If  free  then  allot  that  file  in  those  continuous  blocks  and  update  the  directory structure.</li>

   <li>else repeat step 1</li>

   <li>If no continuous blocks are free then ‘no enough memory error’</li>

   <li>The Directory  Structure  should  contain  Filename,  Starting  Block,  length  (no.  of blocks)</li>

  </ol></li>

 <li>For Linked Allocation- For each file do the following

  <ol>

   <li>Generate a random number between 1 to ‘n’ blocks.</li>

   <li>Check that block is free or not.</li>

  </ol></li>

</ol>

<ul>

 <li>If free then allot it for file. Repeat step 1 to 3 for the needed number of blocks for file and create     linked     list     in     Main     memory     using     the     field     “Link     to  Next File block”.    Update  the  Directory  entry  which  contains  Filename,  Start  block  number,  Ending Block Number.</li>

</ul>

<ol>

 <li>Display the file  blocks  starting  from  start  block  number  in  Directory  upto  ending block  number  by  traversing  the  Main  memory  Linked  list  using  the  field  “Link  to  Next File block”.</li>

</ol>

20.For Indexed Allocation – For each file do the following

<ol>

 <li>Generate a random number between 1 to ‘n’ blocks for index block.</li>

 <li>Check if it is free else repeat index block selection</li>

</ol>

<ul>

 <li>Generate needed  number  of  free  blocks  in  random  order  for  the  file  and  store  those block numbers in index block as array in File block table array.  Display the Directory structure which contains the filename and index blocknumber. Display the File Details by showing the index block number’s File Block Table.</li>

</ul>

SAMPLE INPUT &amp; OUTPUT:




Main Memory size: 500

Size of each block in the disk: 10 KB

Number of files to be allocated: 5

Name of the File1: ****

Size of the file1: ****

<ul>

 <li>•</li>

</ul>




FILE ALLOCATION TECHNIQUES

<ol>

 <li>Contiguous</li>

 <li>Linked</li>

 <li>Indexed</li>

</ol>




Choose the Allocation scheme: 1




CONTIGUOUS ALLOCATION

Directory

File Name    Start    length

*****        ***      ***

*****        ***      ***

<ul>

 <li></li>

 <li></li>

 <li></li>

</ul>

*****        ***      ***

Choose the Allocation scheme: 2




LINKED ALLOCATION




Directory

File Name    Start    End

*****        ***      ***

*****        ***      ***

<ul>

 <li></li>

 <li></li>

 <li></li>

</ul>

*****        ***      ***




Individual File listing




File name   Data-block 1    Data-block j     Data-block k Data-block l Data-block final







Choose the Allocation scheme: 3




INDEXED ALLOCATION




Directory

File Name    Indexed Block

*****         ***

*****         ***

<ul>

 <li></li>

 <li></li>

 <li></li>

</ul>

*****         ***




Display the Index table for all the files in the following manner

File Name      Block Indexed

***                Data-block 1                      Data-block j

Data-block k

Data-block l

Data-block final

<ul>

 <li></li>

 <li></li>

</ul>