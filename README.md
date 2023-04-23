Download Link: https://assignmentchef.com/product/solved-2110215prog-lab1-object-oriented-programming
<br>
<h1>Instruction</h1>

<ol>

 <li>Click the provided link on CourseVille to create your own repository.</li>

 <li>Open Eclipse and then “File &gt; new &gt; Java Project” and set project name in this format</li>

</ol>

<strong>2110215_Lab1_2021_1_{ID}_{FIRSTNAME}</strong>

<ul>

 <li>Example:<strong> 2110215_Lab1_2021_1_6331234521_Jotaro</strong>.</li>

</ul>

<ol start="3">

 <li>Initialize git in your project directory ○ Add .gitignore.

  <ul>

   <li>Commit and push initial codes to your GitHub repository.</li>

  </ul></li>

 <li>Implement all the classes and methods following the details given in the problem statement file which you can download from CourseVille.

  <ul>

   <li>You should create commits with meaningful messages when you finish each part of your program.</li>

  </ul></li>

</ol>

○ Don’t wait until you finish all features to create a commit.

<ol start="5">

 <li>Test your codes with the provided JUnit test cases, they are inside package <strong>grader</strong>

  <ul>

   <li>If you want to create your own test cases, please put them inside package <strong>student</strong></li>

  </ul></li>

</ol>

○ Aside from passing all test cases, your program must be able to run properly without any runtime errors.

<ol start="6">

 <li>After finishing the program, create a UML diagram of all classes in package logic, main and exception using <strong>ObjectAid or another tool (for example: PlantUML) </strong>and put the result image (UML.png) at the root of your project folder.</li>

 <li>Export your project into a jar file called <strong>Lab1_2021_1_{ID}</strong>. Include your source code in the file (DO NOT create a runnable jar) and place it at the root directory of your project.

  <ul>

   <li>Example: <strong>jar</strong></li>

  </ul></li>

 <li>Push all other commits to your GitHub repository</li>

</ol>




<strong> </strong>

<h1>1. Problem Statement: Guild Member Database</h1>

<strong> </strong>

You have been transported into a fantasy world by a magical truck, and was found by a desperate guildmaster who does not know how to use computers. As the only person in this fantasy world who knows how to use a computer, you are asked to implement a system that allows him to manage guild data, including member information and department information.




The program example is shown below. The program should be run from the Main class in the package main.




There are 6 options to do.

<ol>

 <li>View Departments and Members. By default, the first department (department 0) is the Unassigned Department. It is used to contain members that are not assigned to any departments.</li>

 <li>New Department. Creates a new department of the guild. However, department name cannot be duplicate. If a department with a certain name already exists, then it will be rejected.</li>

</ol>

Department name also cannot be blank.

<ol start="3">

 <li>Remove Department. Removes a chosen department. If the removed department has members in it, all of the members in that department will be moved to the unassigned department at index 0.</li>

 <li>New Member. Adds a new guild member to the list by inputting name, job title, and salary. If left blank, the program will input “Anon”, “Adventurer”, and “0” respectively. Then, the user chooses the department to put the new member in.</li>

 <li>Remove Member. Simply removes a member from the guild. Unlike remove department, removed members are permanently removed.</li>

</ol>

<strong> </strong>

The diagram of the program is illustrated below. There are 4 classes: Main, GuildDatabase, Department, and GuildMember.













<ul>

 <li><em>Note that Access Modifier Notations can be listed below </em></li>

 <li><em>Also note that while other methods have been provided, only methods that you have to implement are listed here<strong>  </strong></em></li>

</ul>

<strong><em>+ (public)          </em></strong>

<strong><em># (protected)     </em></strong>

<strong><em>– (private) </em></strong>







<strong>           </strong>

<strong>2.1 Class GuildMember (package logic) </strong>

<h2>2.1.1 Fields</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="312">– String name</td>

   <td width="312">The member’s name. Can contain space. Cannot be blank. If blank, will be set to “Anon”.</td>

  </tr>

  <tr>

   <td width="312">– String jobTitle</td>

   <td width="312">The member’s job title. Can contain space. Cannot be blank. If blank, will be set to “Adventurer”.</td>

  </tr>

  <tr>

   <td width="312">– String myDepartment</td>

   <td width="312">The member’s department.</td>

  </tr>

  <tr>

   <td width="312">– int salary</td>

   <td width="312">The member’s salary. Must be greater than 0 and lesser than 100000. </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h2>2.1.2 Constructors</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="312">+ GuildMember(String, String, int)</td>

   <td width="312"><strong>/*Fill Code*/</strong>Initialize <strong>all fields</strong>. For Department, set it as “Unassigned” here. <strong>Note: You should use setter to set the value of all fields in order to handle negative value case and special case. </strong></td>

  </tr>

 </tbody>

</table>

<h2>2.1.3 Methods</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="312">+ void setName(String)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>This method will set name of the member. If the String is empty, the method will set the name as “Anon”.<strong> </strong><strong>Hint: There is a non-static method called isBlank() in the String class. It returns true if a String consists of only whitespace. </strong><strong> </strong><strong>Example: </strong><strong>String exampleString = “ “; exampleString.isBlank() will return true. </strong></td>

  </tr>

  <tr>

   <td width="312">+ void setJobTitle(String)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>This method will set the job title of the member. If the String is empty, the method will set the job title as “Adventurer”.<strong> </strong></td>

  </tr>

  <tr>

   <td width="312">– void setSalary(int)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>This method will set the salary of the member. If the salary is less than 0, it will be set as 0. If the salary is greater than 100000, it will be set as 100000.</td>

  </tr>

  <tr>

   <td width="312">Getter &amp; Setter methods for all remaining variables</td>

   <td width="312"><strong>/*Fill Code*/</strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>2.2 Class <em>Department (package logic)</em> </strong>

<h2>2.2.1 Fields</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="312">– String name</td>

   <td width="312">The name of the department. It should never be empty.</td>

  </tr>

  <tr>

   <td width="312">– ArrayList&lt;GuildMembers&gt; departmentMembers</td>

   <td width="312">The GuildMembers in this department, contained in a list.</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h2>2.2.2 Constructors</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="312">+ Department(String)</td>

   <td width="312"><strong>/*Fill Code*/</strong>Initialize the list, as well as set the name of the department. <strong>Note: You should use setter to set the value of all fields in order to handle negative value case and special case. </strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h2>2.2.3 Methods</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="312">+ boolean setName(String)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>Set the name of the department and returns</td>

  </tr>

  <tr>

   <td width="312"></td>

   <td width="312">whether or not the name change was a success.–          If the name is not blank, then change the department name and return true.–          If the name is blank, then <strong>DO NOT</strong> change the department name and return false.</td>

  </tr>

  <tr>

   <td width="312">+ String getName()</td>

   <td width="312"><strong>/*Fill Code*/ </strong>Returns the name of the department.</td>

  </tr>

  <tr>

   <td width="312">+ void addMember(GuildMember)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>Add the given member to the list of members, as well as call setMyDepartment(String) to set their department to match this department’s name.</td>

  </tr>

  <tr>

   <td width="312">+ voidaddMultipleMembers(ArrayList&lt;GuildMembe r&gt;)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>Add all the members in the given arraylist to this list. Make sure you call setMyDepartment(String) to set all of their deparments to match this department’s name.</td>

  </tr>

  <tr>

   <td width="312">+ GuildMember removeMember(int)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>Removes a member from the given index from the list of members, and return the removed member.</td>

  </tr>

  <tr>

   <td width="312">+ GuildMember getMember(int)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>Returns a member from the given index.</td>

  </tr>

  <tr>

   <td width="312">+ ArrayList&lt;GuildMember&gt; getAllMembers()</td>

   <td width="312"><strong>/*Fill Code*/ </strong>Returns all members in the department.</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h2><strong>2.3 Class GuildDatabase (package logic) </strong></h2>

<h3>2.3.1 Fields</h3>

<table width="624">

 <tbody>

  <tr>

   <td width="312">– ArrayList&lt;Department&gt; myDepartments</td>

   <td width="312">The list of departments contained in this database.</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h3>2.3.2 Constructors</h3>

<table width="624">

 <tbody>

  <tr>

   <td width="312">+ GuildDatabase()</td>

   <td width="312"><strong>/*Fill Code*/</strong>Initialize myDepartments as an empty ArrayList.</td>

  </tr>

 </tbody>

</table>

<strong>           </strong>

<h3>2.3.3 Methods</h3>

<table width="624">

 <tbody>

  <tr>

   <td width="312">+ boolean createDepartment(String)</td>

   <td width="312"><strong>/*Fill Code*/</strong>Attempts to create a new department with the given name. Returns true or false depends on whether or not a department was successfully created.–          If the department’s name duplicates another department inside myDepartments, <strong>DO NOT</strong> create the department and return false.–          Otherwise, create a new department with the given name and return true.</td>

  </tr>

  <tr>

   <td width="312">+ boolean isExists(String)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>This method runs a check with all departments currently in the databas, using the String given.–          If there is a department with the same name as the given name, return true.–          If there are no departments with the same name as the given name, return false.</td>

  </tr>

  <tr>

   <td width="312">+ ArrayList&lt;GuildMember&gt; removeDepartment(int)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>Remove a department from the given index, and return a list of all members that was in that department before it got removed.<strong> </strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>           </strong>

<h2><strong>2.4 Class Main (Static class): (package Main) </strong></h2>

Details on DuplicateGuildNameException and EmptyGuildNameException will be given to you in the next part.

<h3>2.4.1 Fields</h3>

<table width="624">

 <tbody>

  <tr>

   <td width="312">+ <u>GuildDatabase myDatabase</u> </td>

   <td width="312"><strong>/*Fill Code*/ </strong>The database system.</td>

  </tr>

  <tr>

   <td width="312">+ <u>Scanner kb</u></td>

   <td width="312"><strong>/*Fill Code*/ </strong>Scanner for getting input.</td>

  </tr>

 </tbody>

</table>

2.4.2 Constructors

This class does not need a constructor.

<h3>2.4.3 Methods</h3>

<table width="624">

 <tbody>

  <tr>

   <td width="312">public static boolean addDepartment(String)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>Create a new department using the given name. Returns true or false depending on whether or not the department is successfully created.–          If the given name is blank, <strong>DO NOT</strong> create the department. Throw EmptyGuildNameException and return false, as well as print the exception to tell the user that the name cannot be blank.–          If the given name duplicates a department’s name that already exists, <strong>DO NOT</strong> create the department. ThrowDuplicateGuildNameException and return false, as well as print the exception to tell the user that the name cannot be duplicate.–          Otherwise, create the department and return true.NOTE: Program should still be running after throwing exception. It should return you to the main menu. </td>

  </tr>

  <tr>

   <td width="312"></td>

   <td width="312">NOTE 2: Don’t throw exceptions in the method’s declaration. Instead, you should use try/catch to throw exceptions here.</td>

  </tr>

  <tr>

   <td width="312">public static voidremoveDepartmentFromDatabase(int)</td>

   <td width="312"><strong>/*Fill Code*/ </strong>Remove a department at the given index from the database, and put all the members that used to be in that department into the Unassigned department, which can be called with the getUnassignedDepartment() method. Finally, confirm the user the number of members that are moved to the unassigned department.</td>

  </tr>

 </tbody>

</table>




<h2><strong>2.5 Exception Classes (package exception) </strong></h2>

There are two exception classes provided for you in the package exception.

<ul>

 <li>EmptyGuildNameException should be thrown when inputting an empty guild name. When printed, it will display an error message that says guild name should not be empty.</li>

 <li>DuplicateGuildNameException should be thrown when inputting a duplicate guild name. When printed, it will display an error message that says guild name should not be duplicate.</li>

 <li>To throw an exception, do:</li>

</ul>

o throw new EmptyGuildNameException(); o throw new DuplicateGuildNameException();

<strong> </strong>

<h1>3. Test Scenario</h1>

(User input is in green.)
















<h1>4. Exception Scenarios</h1>

Throwing DuplicateGuildNameException







Throwing EmptyGuildNameException


