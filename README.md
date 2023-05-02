Download Link: https://assignmentchef.com/product/solved-cop2805c-java-programming-2-project-2
<br>
Design a class ​<strong>Student</strong>​ that contains the following members:

<ul>

 <li>String fields ​<strong>firstName, lastName</strong>​ and ​<strong>status</strong>​.</li>

 <li>char field <strong>letterGrade</strong>​ .​</li>

 <li>double fields ​<strong>grade1, grade2, grade3</strong></li>

 <li>double field ​<strong>average</strong></li>

 <li>A two-argument constructor that takes ​<strong>firstName </strong>​and​<strong> lastName </strong>​as parameters.</li>

 <li><strong>computeAverage</strong> ​ Take into account that you will have different number of grades​      depending on the student.</li>

 <li><strong>computeStatus</strong>​ method (If ​<strong>average</strong>​ is &lt; 70, the status will be “Failing”. Otherwise, the status is “Passing”)</li>

 <li><strong>computeLetterGrade </strong>​method (If average &gt;= 90 letterGrade is ‘A’, If average &gt;= 80 letterGrade is ‘B’, If average &gt;= 70 letterGrade is ‘C’, If average &gt;= 60 letterGrade is ‘D’, else letterGrade is</li>

</ul>

‘F’)

<ul>

 <li><strong>get </strong>​and ​<strong>set</strong>​ methods for ​<strong>all</strong>​</li>

</ul>

Design a class ​<strong>StudentList</strong>​ that contains the following members:

<ul>

 <li>An ​<strong>ArrayList</strong>​ of Student objects ​<strong>students</strong>​.</li>

 <li><strong>readStudents</strong> method that prompts the user for an input file name (use JFileChooser) and reads​ the contents of the input file into ​<strong>students</strong>​. You can expect the file to be a text file with the following format:</li>

</ul>

firstName|lastName|Grade1|Grade2         //Student 1  firstName|lastName|Grade1|Grade2|Grade3      //Student 2

firstName|lastName|Grade1                                  //Student 3

firstName|lastName                                              //Student 4

<strong>    … </strong>

Sample input file contents:

Michael|Corleone|78.6|99.7

Luca|Brasi|90.5|100|100

Phillip|Tattaglia|78.1

Kay|Adams

<strong> </strong><strong> </strong>

<strong>Notes: </strong>

<ul>

 <li>Use ​<strong>Split()</strong>​ method to parse the input.</li>

 <li>The file could have any length; therefore, you cannot make assumptions about how many students you’ll find in the file.</li>

 <li>You can assume that the information for every student will include firsName, LastName and between 0 and 3 grades.</li>

 <li>Need to populate the ​<strong>average</strong>​, ​<strong>status</strong>​ and ​<strong>letterGrade</strong>​ fields as appropriate.</li>

</ul>




<ul>

 <li><strong>saveStudentsToDB</strong>​ method​ ​that prompts the user for an DataBase file name (use JFileChooser) and writes the contents of ​<strong>students</strong>​ to the DB. The database will contain the table ​<strong>StudentsTbl </strong>with the following columns: ​<strong>ID (ignore),</strong>​ ​<strong>FirstName, LastName, Grade1, Grade2, Grade3, Average, Status </strong>​and​</li>

 <li><strong>findStudent</strong>​ method that prompts the user for a student name and last name and shows a message indicating that the student was either found or not found ​in the DB​.(use JOptionPane with a text field(s) and OK and Cancel buttons). Continue asking the user until the user presses ​<strong>Cancel</strong>​.</li>

 <li><strong>writeStudents</strong>​ method that prompts the user for an output file name (use JFileChooser) and writes the contents of the ​<strong>StudentsTbl </strong>​from the DB to the output file with the following format:</li>

</ul>

Name               Grade 1           Grade 2           Grade 3           Average           Letter Status

Grade

Michael Corleone       100.00             100.00             100.00             100.00                 A       Passing

Phillip Tatagliaz         60.00                 60.00               60.00               60.00                 F         Failing




<ul>

 <li><strong>writeSortedStudents</strong>​ method that prompts the user for an output file name (use JFileChooser) and writes the contents of the ​<strong>StudentsTbl </strong>​from the DB to the output file ​in ascending order of average​ (use ​<strong>order by</strong>​ SQL clause) with the following format:</li>

</ul>

Name               Grade 1           Grade 2           Grade 3           Average           Letter Status

Grade

Michael Corleaone      100.00             100.00             100.00             100.00                 A       Passing

Julio Perez      60.00                 60.00               60.00               60.00                 F      Failing




Create a class ​<strong>TestStudents</strong>​ to test your work. This class will have a main that looks exactly like this:

public static void main(String[] args) {

StudentList studentList = new StudentList();

studentList.readStudents(); studentList.saveStudentsToDB();     studentList.writeStudents(); studentList.writeSortedStudents(); studentList.findStudent(); }











