# UI-Layer-Assignment
Assignment

                                                                  JavaScript Assignment
                                                                  

Que-1:  Write script for following methods of Array object: 
Ans:
a. Find() 
b. Filter() 
c. Map() 
d. Reduce() 
e. Slice() 
f. Splice()

const student = [
    {id: 101, name: 'John', age: 22},
    {id: 102, name: 'Julie', age: 23},
    {id: 103, name: 'Tom', age: 19},
    {id: 104, name: 'Alina', age: 24},
    {id: 105, name: 'Chris', age: 20},
    {id: 106, name: 'Jack', age: 18}
  ];
  
  //find() method-------------------------------------------------------------------------------------
  const studentName = student.find( ({ name }) => name === 'Chris' );
  
  console.log(studentName); 

  //filter() method-------------------------------------------------------------------------------------

  const studentAge = student.filter(({ age }) => age > 20); 
  console.log("Student age is", studentAge);

  //map() method-------------------------------------------------------------------------------------

  const array1 = [1, 4, 9, 16];
  const numbers = array1.map(x => x * x);
  console.log("Square of given array is: ", numbers);
  
  //reduce() function-------------------------------------------------------------------------------------
  array1.reduce(

    ( previousValue, currentValue ) => previousValue + currentValue,
    0
  );

  console.log(array1);

  //slice() method-------------------------------------------------------------------------------------

  array2 = ['New York', 'Paries', 'Mumbai', 'Tokyo', 'Las Vegas'];      
  // [1:New York, 2:Paries, 3:Mumbai, 4:Tokyo, 5: Las Vegas]
  console.log("After slicing an array: ", array2.slice(3)); //start from 3rd index
  console.log("After slicing an array: ", array2.slice(1, 4));
  //slice(start, end)

  // splice() method (can remove or replace element)-------------------------------------------------------

  array2.splice(1, 0, 'Delhi'); //new element added in an array at index[1]
  console.log(array2);

  array2.splice(2, 1);      //splice(start[index], deletedItem[index])- index[2] element will be removed from array
  console.log(array2);


----------------------------------------------------------------------------------------------------------------------------------------

Que-2: Study closure in JavaScript and write script for the same
Ans:



----------------------------------------------------------------------------------------------------------------------------------------

Que-3: Write a JavaScript function to merge two arrays and removes all duplicates elements 
Test data :
 var array1 = [1, 2, 3]; 
var array2 = [2, 30, 1]; 
console.log(merge_array(array1, array2)); 
[3, 2, 30, 1]


Ans:

var array1 = [1, 2, 3];
var array2 = [2, 30, 1];

  const array3 = (arr) => {
    return Array.from(new Set(array1.concat(array2)));
  }
  
  console.log('output', array3());

----------------------------------------------------------------------------------------------------------------------------------------

Que-4: Write a pattern that matches e-mail addresses. The personal information part contains the following ASCII characters. 
• Uppercase (A-Z) and lowercase (a-z) English letters. 
• Digits (0-9). 
• Characters ! # $ % & ' * + - / = ? ^ _ ` { | } ~ 
• Character . ( period, dot or full stop) provided that it is not the first or last character and it will not come one after the other.
Ans-

//valid email program

function valid_email(str){
            
var mailformat = /^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/;  
            
if(mailformat.test(str)){ 
    
    console.log("Valid email address!");  
    } else {  
        console.log("You have entered an invalid email address!");  
        }
}

    valid_email('me-info@example.com');
    valid_email('something.something.com')


----------------------------------------------------------------------------------------------------------------------------------------

Que-5: Write a JavaScript function to get the values of First and Last name of the following form: 
Ans:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Return first and last name from a form</title>
</head>
<body>
    <form id="form1" onsubmit="getFormvalue()">
        First name: <input type="text" name="fname" value="David"><br>
        Last name: <input type="text" name="lname" value="Beckham"><br>
        <input type="submit" value="Submit">
</body>
<script>
function getFormvalue(){

  var formVal=document.getElementById("form1");
  
  for (var i=0;i<formVal.length;i++){

    if (formVal.elements[i].value!='submit'){

        console.log(formVal.elements[i].value);
    }  
 }
}
</script>
</html>


----------------------------------------------------------------------------------------------------------------------------------------

Que-6: Write a JavaScript program to remove items from a dropdown list.
Ans: 

<!DOCTYPE html>
<html><head>
<meta charset=utf-8 />
<title>Remove items from a dropdown list</title>
<link rel="stylesheet" href="https://codepen.io/nullobject/pen/cngzI">
</head>
<body>
    <form>
        <select id="colorSelect">
        <option>Red</option>
        <option>Green</option>
        <option>White</option>
        <option>Black</option>
        </select><br><br>
        <input type="button" onclick="removeItem()" value="Select and Remove">
    </form>
    <script>
        function removeItem(){
            var rmvItem = document.getElementById("colorSelect");
            rmvItem.remove(rmvItem.selectedIndex);
            }
        
    </script>
</body>
</html>

----------------------------------------------------------------------------------------------------------------------------------------

Que-7: Write a JavaScript program to highlight the bold words of the paragraph, on mouse over a certain link. Test data: Link text is – Click here to highlight bold words.
Ans: 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <a href="#" onMouseOver="showBold()" onMouseOut="showNormal()">Click here to highlight bold words.</a>
    <p>Lorem ipsum dolor sit amet <strong>consectetur adipisicing</strong> elit. 
        <strong>Libero </strong>minima veritatis hic, fugit <strong>deleniti</strong> magni quia. 
        Quam quo beatae et <bold>distinctio veniam possimus</bold>, qui optio molestiae quasi, 
        incidunt, <strong>repudiandae</strong> dolore.</p> 

    <p>Lorem, ipsum dolor sit amet <strong>consectetur adipisicing</strong> elit. 
        Magnam excepturi commodi <strong>corporis</strong> aperiam ex vero culpa 
        aliquid debitis <strong>doloremque doloribus</strong> earum ab cum beatae consectetur 
        cupiditate, optio odio quod adipisci?</p>
</body>

<script>

    function showBold(){
        var showBoldText = document.getElementsByTagName("strong");
        for (var i = 0; i < showBoldText.length; i++) {
        showBoldText[i].style.backgroundColor = "green";
        }
    }

    function showNormal(){
        var showNormalText = document.getElementsByTagName("strong");
        for (var i = 0; i < showNormalText.length; i++) {
        showNormalText[i].style.backgroundColor = "black";
        }
    }
</script>
</html>


----------------------------------------------------------------------------------------------------------------------------------------

Que-8: Write a JavaScript function to get the month name from a particular date. 
Test Data : console.log(month_name(new Date("10/11/2009"))); 
console.log(month_name(new Date("11/13/2014"))); 

Output : 
"October" 
"November”

Ans: 

var month = function(date){
    allMonths = [ "January", "February", "March", "April", "May", "June", "July", 
                  "August", "September", "October", "November", "December" ];
                  
      return allMonths[date.getMonth()];
    };

    console.log(month(new Date("10/11/2009")));
    console.log(month(new Date("11/13/2014")));


----------------------------------------------------------------------------------------------------------------------------------------

Que-9:  Write a JavaScript function to test whether a date is a weekend. Go to the editor 
Note : Use standard Saturday/Sunday definition of a weekend. 
Test Data : 
console.log(is_weekend('Nov 15, 2014')); 
console.log(is_weekend('Nov 16, 2014')); 
console.log(is_weekend('Nov 17, 2014')); 
Output : 
"weekend" 
"weekend" 
Undefined

Ans:


var is_weekend = function(date){
    var dt = new Date(date);
     
    //if(dt.getDay() == 5 || dt.getDay() == 0){ // including weekend as sat & sun
    if(dt.getDay() == 6 || dt.getDay() == 0){  //only on Sunday

            return "Weekend!";
    } else{
        return "Week Day!";
    }
}

console.log(is_weekend('Nov 15, 2014')); 
console.log(is_weekend('Nov 16, 2014')); 
console.log(is_weekend('Nov 17, 2014')); 


----------------------------------------------------------------------------------------------------------------------------------------

Que-10: Write a JavaScript program to display the reading status (i.e. display book name, author name and reading status) of the following books.
Sample Object: 
var library = 
[ 	{ author: 'Bill Gates', title: 'The Road Ahead', readingStatus: true }, 
{ author: 'Steve Jobs', title: 'Walter Isaacson', readingStatus: true }, 
{ author: 'Suzanne Collins', title: 'Mockingjay: The Final Book of The Hunger Games', readingStatus: false }
]; 
Ans: 

var library = [ 
    {
        author: 'Bill Gates',
        title: 'The Road Ahead',
        readingStatus: true
    },
    {
        author: 'Steve Jobs',
        title: 'Walter Isaacson',
        readingStatus: true
    },
    {
        author: 'Suzanne Collins',
        title: 'Mockingjay: The Final Book of The Hunger Games', 
        readingStatus: false
    }
];


function bookReadingStatus(status){
    for(var i = 0; i < library.length; i++){
        var status = library[i].author + " of " + library[i].author + " by " + library[i].title;
        
        if(library[i].readingStatus == true){
            console.log("Yo've completed the reading ", status);
        }else{
            console.log("Yo've incompleted the reading ", status);
        }
    }
}

console.log(bookReadingStatus());


----------------------------------------------------------------------------------------------------------------------------------------

Que-11: Write a JavaScript program to create a Clock. 
Note: The output will come every second. 

Expected Console Output: 
"14:37:42" 
"14:37:43" 
"14:37:44" 
"14:37:45" 
"14:37:46" 
"14:37:47"

Ans:


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  
  <p id="timerClock"></p>

  <script>

    function checkTime(i) {
      if (i < 10) {
        i = "0" + i
      };
      return i;
  }
    
  function myClock(){
    const today = new Date();
  
    let hh = today.getHours();
    let mm = today.getMinutes();
    let ss = today.getSeconds();
  
    mm = checkTime(mm);
    ss = checkTime(ss);
    document.getElementById("timerClock").innerHTML = "Current Time : " + hh + ":" + mm + ":" + ss;
    setTimeout(myClock, 1000);
  }
  
  console.log(myClock());
  </script>
</body>
</html>


----------------------------------------------------------------------------------------------------------------------------------------

Que-12:  Write a JavaScript program to sort an array of JavaScript objects. 

Sample Object: 
var library = 
[ 	{ title: 'The Road Ahead', author: 'Bill Gates', libraryID: 1254 }, 
{ title: 'Walter Isaacson', author: 'Steve Jobs', libraryID: 4264 }, 
{ title: 'Mockingjay: The Final Book of The Hunger Games', author: 'Suzanne Collins', libraryID: 3245 }
];
Ans: 

var library = [ 
    {
    title: 'The Road Ahead',
    author: 'Bill Gates',
    libraryID: 1254
    },
    {
    title: 'Walter Isaacson',
    author: 'Steve Jobs',
    libraryID: 4264
    },
    {
    title: 'Mockingjay: The Final Book of The Hunger Games',
    author: 'Suzanne Collins',
    libraryID: 3245
    }
];

library.sort(function (a, b) {
    return a.libraryID - b.libraryID;
  });

//var newobj = library.sort('libraryID', true);

console.log("sort of an array : ", library);

----------------------------------------------------------------------------------------------------------------------------------------

Que-13: Study Promises in JavaScript and provide script for the same
Ans:


