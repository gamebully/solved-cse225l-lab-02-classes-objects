Download Link: https://assignmentchef.com/product/solved-cse225l-lab-02-classes-objects
<br>



Recall the class for dynamic array we developed in our 2<sup>nd</sup> lecture. In this lab session, you will implement and test that class.

<strong>Before you begin:</strong> Create a C++ project. Then create a header file and a source file for your project. Follow the steps below to create files.

<ol>

 <li>Create a header file.

  <ol>

   <li>File ⇒ New ⇒ Select C/C++ header. Select Go ⇒ Next.</li>

   <li>Click the browse button beside the textbox labelled “Filename with full path”. A window appears. In the textbox labelled “File name”, type in the name you want to assign to the header file (in this case dynarr.h). Select Save ⇒ select All ⇒ select Finish.</li>

   <li>Under the “Management” pane ⇒ Choose “Projects” tab ⇒ Expand the project node ⇒ Expand “Headers” node. You will see the file you just created. It is mostly blank except for a few lines of code. It is time to add your own code to it. For your convenience, the content of this file is already provided with this manual (refer to the table in the opposite page). Add the content of dynarr.h just before the #endif</li>

  </ol></li>

 <li>Next, create the source file

  <ol>

   <li>File ⇒ New ⇒ Select C/C++ source. Select Go ⇒ Next.</li>

   <li>Select “C++” ⇒</li>

   <li>Click the browse button beside the textbox labelled “Filename with full path”. A window appears. In the textbox labelled “File name”, type in the name you want to assign to the source file (in this case dynarr.cpp). Select Save ⇒ select All ⇒ select Finish.</li>

   <li>Under the “Management” pane ⇒ Choose “Projects” tab ⇒ Expand the project node ⇒ Expand “Sources” node. You will see the file you just created. It is completely blank. It is time to add your own code to it. For your convenience, the content of this file is already provided with this manual (refer to the table in the opposite page). Add the content of dynarr.cpp to the newly created file.</li>

  </ol></li>

 <li>In the opposite page, will find some tasks that you have to perform using the code provided. You have to modify the file main.cpp and perform these task in that file.</li>

 <li>To build the program, select “Build” menu ⇒</li>

 <li>To run the program, select “Build” menu ⇒</li>

</ol>




<table width="0">

 <tbody>

  <tr>

   <td width="334"><strong>dynarr.h </strong> #ifndef DYNARR_H_INCLUDED #define DYNARR_H_INCLUDED class dynArr{private:int *data;     int size;public:dynArr();     dynArr(int);     ~dynArr();     void setValue(int, int);int getValue(int);};#endif // DYNARR_H_INCLUDED </td>

   <td width="378"><strong>dynarr.cpp </strong> #include “dynarr.h” #include &lt;iostream&gt; using namespace std; dynArr::dynArr(){     data = NULL;     size = 0;}dynArr::dynArr(int s){data = new int[s];     size = s;}dynArr::~dynArr(){delete [] data;} int dynArr::getValue(int index){return data[index];}void dynArr::setValue(int index, int value){data[index] = value;} </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong><u>Tasks:</u></strong>

<strong> </strong>

<strong>Task 1:</strong> In the driver file (main.cpp), perform the following sub-tasks.

<ol>

 <li>Create two objects of this class, one with no constructor argument and one with the argument 5.</li>

 <li>Take five input values from the user and store them in the array inside the second object using the set method.</li>

 <li>For the second object, print all the values you just stored.</li>

</ol>

Note that, you cannot assign anything in the first object since the array inside it has size 0. Neither can you change the size of this array to some other size.

<strong> </strong>

<strong>Task 2: </strong>Modify the header and the source files. Add a member function <strong>void allocate(int s)</strong> which allows you to change the size of the array. Make sure that memory is not leaked.




<strong>Task 3: </strong>Modify the header file and the source files again, so that it works for two dimensional array where all the rows are the same size. The user will specify the number of rows and columns as well as the content of the array, which you will take as input from user in the main function.