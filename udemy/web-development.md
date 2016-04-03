###Hosting Site: `https://www.ecowebhosting.co.uk/cp/webdevcourse`

Site link http://217.199.187.191/samanthalanasa.com/

if you need help with code `jsbin.com`

#HTML

its good to tell the doc type `<!doctype html>`

anything in `<>` is a `tag`

the first section of a page is the `<head>` 

`<title>` is what appears in browser

`<meta tag>`; `charset` character set, its important to set a char set `utf-8` is fine for now

view port is important when desiging for mobile to shut off zoom, sets width to be device width. 

div is a division of a page, you normally separate you page into different divs

My first HTML Site
http://sites.codeschool.org.uk/?site=lovethemapples

#CSS
 <p>A <span class="definition">class</span> is name for a certain type of text with special instructions or styles</p>
		
		<p>more text</p>
	
	</div>
	
	<div class="greenbox">
		
		<p>The difference between <span class="definition">class</span> and <span class="definition">IDs</span> is that ids you aren't supposed to use more than once.</p></div>
	
	clearing div an empty div thats only purpose is to break floats and start them again. you can clear: left, right, or both. Usually you want to clear both.
`position:relative;` meants you can move it around to where it would otherwise be. if we want to move it to the right, we move it to the left. If want to move it 100px to the right `left:100px;` because we're adding a margin of 100px. when you move things around this way it will move on top of other elements. add a negative margin `-50px` to move it up.

`position:absolute;` divs ignore presence of other divs

`position:fixed;` will stay in one palce upon scroll

`position:static;` 

zed index or `z-index` value is a layering tool that allows you to put one div oon top of another, the one with the larger value goes on top. for this to work each element has to have a position.

margins

`margin:50px 100px 30px 10px;` starts as top 50px, right 100px, bottom 30px, and left 10px, as it goes in a clockwise motion

`margin:left;` to set a specific margin

`p` tag has padding built in

#Building A website

###Div
`<div id="container">` putting your all of your site in a container is good practice because it give you control of what styles are in your website

###Topbar
create your topbar with a style `		#topbar{
			background-color:#7A0000;
			height:40px;
			width:100%;
		}`
		
To rid the padding around the topbar use `body{
			margin:0px;
		}`
		
create a div for the logo with ID `#logodiv{
			padding-top:8px;
			float:left;
		}`. to have other content next to it float left
		
create a div 

	#topmenudiv ul{
			margin:0;
			padding:0;
			
		}

		#topmenudiv li{
			float:left;
			list-style:none;
			font-size:12px;
			font-weight:bold;
			border-right:1px #990000 solid;
			height:100%;
			padding:14px 14px 12px 14px;
		}
and add an unordered list to create the nav menu 
	
				<div id="topmenudiv">
					
					<ul>
						<li>News</li>
						<li>Sport</li>
						<li>Weather</li>
						<li>iPlayer</li>
						<li>TV</li>
						<li>Radio</li>
						<li>More..</li>
					</ul>
			
				</div>
		
		
create a search bar with

	#searchdiv{
			float:left;
			padding:7px 7px 7px 6px;
		}
		
		#searchdiv input{
			height:20px;
			border:none;
			padding-left:7px;
			font-size:12px;
			background-image:url(images/search.png);
			background-size:15px;
			background-repeat:no-repeat;
			background-position:130px;
		}

and then
	
	<div id="searchdiv">
					<input type="text" placeholder="Search">
				</div>
				
###Middle Content - to set a fixed width
create a div inside the top bar div with class `.fixedwidth{
			width:1100px;
			margin:0 auto;
		}`
		
###breaking floats

to break between to objects like nav bar and header break floats by creating div between the two `<div class="break"></div>`

with class instructions 
			
			.break{
			clear:both;
		}
		
		
####sd

`padding-top:5px !important!;` the important command should be used sparingly to override any conflicting commands for the same element

####Link Tags
`<link rel="stylesheet" type="text/css" href="style.css"/>`
		
		

#Javascript

Its conventional to have
	
	<script type="text/javascript">
	
	</script>
	
###Accessing Elements 
	
	<p id="text">some text</p>`
	
	<script type="text/javascript">
	
		document.getElementById("text").innerHTML="Some more text";
	
	</script>

`document` refers to the whole page itself

use `.` to refer to a sub element with the document

always start javascript functions with a small letter then camelcase: `getElementByID` and use `("text")` to speficy that element.

use `.innerHTML`to get content in the HTML


use `="Some more text"` to se content of the HTML

	// This is a Comment //
	
	/* This is a multiline comment
	
	*/
	
	
###Responding to a Click
	<button id="myButton">You know you want to click me</bottom>
	
	<script type="text/javascript">
	
		document.getElementById("myButton").onclick=function() {
			
			alert("HI!");
		}
	
	</script>
	
###Changing Website Content

	<button id="textChanger">Change first div text</button>
		
	<div id="firstdiv">This is some text</div>
	
	<button id="textAppender">Append some text</button>
	
	<div id="secondDiv">Javascript is...</div>
	
	<button id="textCreator">Create some Text</button>
	
	<div id="emptyDiv"></div>	
	
	<script type="text/javascript">
	
		document.getElementById("textChanger").onclick=function() {
			
			document.getElementById("firstdiv").innerHTML="This is Awesome!";
		}
		
		document.getElementById("textAppender").onclick=function() {
			
		document.getElementById("secondDiv").innerHTML=document.getElementById("secondDiv").innerHTML + "great!";
		}
	
	
		document.getElementById("textCreator").onclick=function() {
			
			document.getElementById("emptyDiv").innerHTML="<ul><li>Cat</li><li>Dog</li></ul>";
		}
		
	</script>
	
###Making a Circle Disappear

	<style>
	
		#redCircle{
		border-radius:50%;
		background-color:red;
		width:200px;
		height:200px;
		}
	
	</style>
	
	</head>

	<body>

		<div id="redCircle"></div>
	
		<script type="text/javascript">
	
		document.getElementById("redCircle").onclick=function() {
			
		document.getElementById("redCircle").style.display="none";
		}

		</script>
		
	</body>
	
###Variables

`var divId="redCircle";` 

		<input id="myInput" type="text" value="test" />
	
		<button id="stylesChanger">Change this Text!</button>
	
		<div id="firstDiv"> this is some text</div>
	
		<script type="text/javascript">
	
			var newText=document.getElementById("myInput").value;
	
		document.getElementById("stylesChanger").onclick=function() {
			
			newText=document.getElementById("myInput").value;
			
			document.getElementById("firstDiv").innerHTML=newText;
		}	


here we're using text input as a variable the the user can control. using a javascript variable of `newText` that we're setting as a value of the input value to change the HTML of the `firstDiv` div.

###Arrays
Arrays are very similar to variables but they allow you to store several different values within the same object.

`var myArray=new Array();` is how you create an Array. `myArray` is the name here.

You can set specific values of the array to have values of their own.
`myArray[0]="pizza";` where myArray equals pizza. so `myArray` can have lots of different values and infinite numbers which can be set to a value of their own. 

You might use this to list all the users registered on your database, or the divs in a particular webpage, etc.

Another way to write arrays is `myOtherArray=["rain","sunshine"];`

####Console.log

The console log is good for debugging and finding out what the value of a specifc array is.

####Teniques to Add and Remove Elements from Arrays

######Push 
Allows you to add an element at the end of an array. `myOtherArray.push("snow");`

######Splice
A function that Removes elements from the Array. `myOtherArray.splice(1,1);` where *x* is the item number, and *y* is the quantity of items to be removed.

We can also use this command to add elements in the middle of the array `myOtherArray.splice(1,0, "hail");` where `"hail"` will be added before sunshine in the array. and you can add more than one `myOtherArray.splice(2,0, "hail", "cloudy");`


if you created an created an array and you want to knwo how many arrays it has in it you can use the .length command `console.log(myOtherArray.length);`

###If Statements

`==` tests whether or not something is equal to where `=` means something equals.

	var x=2;
	
	if (x==1){
		alert("x is 1!");
	} else{
		alert("x is not 1!");
	}

Another example:
			document.getElementById("myButton").onclick=function() {
			
		if (document.getElementById("weather").value=="rain") {
			
			alert ("it's raining");	
								
		} else {
			
			alert ("it's not raining");
		}
		
		
###Making a Guessing Number Game


######Things we can do with the variable

	var x=5;
	
	alert(x+1);
	
or we can do `alert(3*x);`,`alert(Math.pow(x,2));`,`alert(Math.random());`

the `.random` generated a number between 0 and 1. to do more than that do `x=5*x;`

`x=Math.floor(x)` rounds it down to the nears whole number below x. 

	<p>How man fingers am I holding up?</p>
	<input id="answer" />
	
	<button id="myButton">Guess</button>
	
	
	<script type="text/javascript">
	
		document.getElementById("myButton").onclick=function(){
			
			var x=Math.random();
	
			x=6*x;
	
			x=Math.floor(x);
			
			if (x==document.getElementById("answer").value) {
				
				alert("That's correct!");
				
			} else{
				
				alert("That's wrong! My number was " + x);
			}
			
		}

	</script>

###Loops
A **loop** is doing something several times and *looping* through the results.

	
This is **For Loop**

`for` takes you through a cycle of values of a variable.

`i` is the counter variable, in `i=1`, your setting it to *initial*ly start at *1*.

`i=i<5` or `i=i<=5` sets the upper variable limit. so it wont go over 5.

to set the increments you would use `i=i++` to go up by one. by two `i=i+1` `i=i-1` decrease by 1.

	var myArray=["pizza", "chocolate", "crisps"];
	
	for (var i=0; i<myArray.length; i++) {
		
		alert(myArray[i]);
	}

#####Placing Results on Page

a *string* is a collection of numbers and letters.
	<p id="arrayString"></p>
	

	<script type="text/javascript">
	
	var arrayString=" ";
	
	var myArray=["pizza", "chocolate", "crisps"];
	
	for (var i=0; i<myArray.length; i++) {
		
		arrayString=arrayString+myArray[i]+ ", ";
	}
	
	document.getElementById("arrayString").innerHTML=arrayString;
	
	</script>



