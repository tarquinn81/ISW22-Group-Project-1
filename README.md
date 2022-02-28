# ISW22-Group-Project-1

This is a group assignment so the group should only submit one. Make sure that on the submission all group member names are listed in the Learning Suites Notes area for the assignment.

Create a website that uses the following information to calculate a student’s chance (crude approximation and non-binding) of being accepted into the Information Systems Core program (BSIS).

You will need one html home page only for this assignment.

Make sure the page looks professional. Meeting the requirements will gain 85%. Adding the professionalism is worth 15% of the 100 points so spend the time to make it look very neat, professional, and easy to use.

There should be a link somewhere on this page that will direct the user to https://marriottschool.byu.edu/infosys/ . Make sure that link is either a picture, button, or something visual for the user to click on.

Somewhere on the page include the following:

Program Overview

The BS Information Systems program is available as a four-year traditional degree or as a five-year integrated option where students earn both the BS IS and MISM degrees. The BS IS program is a 64-credit degree including pre-management, junior core, management core, and a capstone.

Curriculum

Information systems students learn to define, develop, and maintain the information system infrastructure that supports the operations of all businesses, governments, and other institutions. The BS Information Systems degree develops the ability to function effectively as a professional, applying state-of-the-art technology in solving business problems. Students are trained in business and information systems and taught to understand complex business environments.

Built on a solid foundation of business courses, the curriculum advances students’ understanding of technologies in the design and development of information systems. They gain technical expertise in systems analysis; systems design and implementation; database development and management; programming; telecommunications networking; 2-tier, 3-tier, and n-tier application development; and web application development.

On this page you will have the following inputs in the html form.

NOTE: Default the drop downs to A’s and the retake checkbox to false (empty). Do this for all of the drop downs and checkboxes.

IS 201 Intro to Management Information Systems Grade and a drop down box (with A, A-, B+, B, B-, C+, C, C-, D+, D, D-, E) and a checkbox asking if this score is a retake.
IS 303 or CS 142 Intro to Computer Programming Grade and a drop down box (with A, A-, B+, B, B-, C+, C, C-, D+, D, D-, E) and a checkbox asking if this score is a retake.
ACC 200 Principles of Accounting Grade and a drop down box (with A, A-, B+, B, B-, C+, C, C-, D+, D, D-, E) and a checkbox asking if this score is a retake.
FIN 201 Principles of Finance Grade and a drop down box (with A, A-, B+, B, B-, C+, C, C-, D+, D, D-, E) and a checkbox asking if this score is a retake.
MKTG 201 Marketing Management Grade and a drop down box (with A, A-, B+, B, B-, C+, C, C-, D+, D, D-, E) and a checkbox asking if this score is a retake.
Text box to enter BYU Overall GPA
Text box to enter BYU Last 30 credits GPA
Button that says CALCULATE
Button that says RESET
Try to make the input area look very nice and clean.



NOTE: If the user clicks on the retake check box then lower the point value for the letter grade by one level (ex. A becomes an A-, A- becomes a B+, etc. )

 

Remember the following grade associations:

A = 4
A- = 3.7
B+ = 3.4
B = 3
B- = 2.7
C+ = 2.4
C = 2
C- = 1.7
D+ = 1.4
D = 1
D- = .7
E = 0
When the page is first displayed (or loaded) or if the user clicks on the RESET button, the IS201 drop down list should have focus.

When the user clicks on the RESET button you should call a JavaScript function called clearCircle() and clear the circle (style.display = "none" and style.fill = "none" for the element), clear the output GPA, clear the overall GPA and the last 30 credits GPA, reset all drop downs to empty and the checkboxes to false, and then set focus to the IS202 drop down.

If the user clicks on the Calculate button, then you should call a JavaScript function called calcGPA() and calculate the GPA using the following information:

IS 201 is worth 20%

IS 303 or CS142 is worth 20%

ACC 200, FIN 201, and MKTG 201 combined are worth 20%

The overall GPA is worth 20%

The last 30 GPA credits is worth 20%

 

Make sure the user has selected a value for each of the drop down list boxes and that a value (don't worry about numeric vs non-numeric) for the overall and last 30 credit GPAs. If they did not enter everything display an alert that says, "You must select an item in each drop down and enter a value in the GPA text boxes!" and set the focus to the IS 201 drop down list box.

Otherwise, grab all of the data and do the calculation.

Then round the data to 2 decimal places.

 

You can try to use the function:

function round(value, decimals) 
{
   return Number(Math.round(value+'e'+decimals)+'e-'+decimals);
}

and call it:

fTotalGPA = round(fTotalGPA, 2);

if fTotalGPA was the variable from the GPA calculation

 

Then if the GPA is 3.7 or above, display a green circle.

If the GPA is 3.4 and above but less than 3.7, display a yellow circle.

Otherwise display a red circle.



This is how you can use the SVG tag to display a circle:

<svg height="100" width="100">
<circle id="myCircle" cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="green" display = "none" /></svg>

And how you can change its color:

document.getElementById("myCircle").style.display = "block";                                         
document.getElementById("myCircle").style.fill="green";

Then display the calculated GPA on the web page somewhere.

Make sure you put in comments in the HTML and the JavaScript.

Include the JavaScript in the HTML in a script tag.

Submit the completed file.
