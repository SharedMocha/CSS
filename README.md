#CSS


Rules:
Never to forget : 
1.ALL HTML ELMENTS ARE BOXEX(SO YOU CAN APPLY BOX PROPETIES), 
2.)ALL DIVS CAN USE POSITION like realtive,aboslute,fixed to be on left,right or anyware. 
3.)ALL HTML ELMENTS WILL HAVE DISPLAY FOR STYLING LIKE inline,inline-block,block etc..
4.) know more on display:grid,flexbox --these are one-dimension meaning only rows
5.) use grids for designing in two dimension--meaning rows and columns---
6.)use hsl color and sans-serif-fonts (ex-arial)-make sure no more than 2 or 3 font-family exists in ui

****MOST IMP -- WHILE YOU CAN USE BOX MODEL,POISTION AND DISPLAY TO PUT ELMENTS-- THERE IS  MORE BETTER WAY --CALLED AS 'CSS GRIDS'--> THIS IS WHAT WE WILL USE as it is 2d -rows and columns

4.)Grids - define your overall html page using grids ->combine rows and columns to get the best  --https://s3.amazonaws.com/codecademy-content/courses/learn-css-grid/lesson-i/css_grid_diagram_2.svg
5.)(you can use grid-template-columns and grodi-template-rows or combine them into one using grid-template- and use repeat, fr,minmax to create rows easily)
6.)**in grids when clubing rows using span along with grid-row and grid-column--** or m,ore easy grid-area which combines grid-row and grid-column..u can use grid-area to show items on top of each other ..like name on top of image..
7.)remember when using grids isntead of giving no of rows and columns-u can give names(grid-template-areas)-. you can give spaces to elments and move entire rows or table -left to right(justify-items,justify-conten) and top to bottom(align-items,align-content)..u can also allign individual cells in grid to elft,right(justify-self),top,bottom(align-self)
8.)in grid you add add rows/columns dynamically too using  (grid-auto-rows,grid-auto-columns,grid-auto-flow) --u need to remove height value from class of g_r_i_d --so it can overfloow
9.)In grid u can remove width --so u can usminmax function--as it helps grid elments to grow or shrink based on content size..
10.) know about box alignment -https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Box_Alignment_in_CSS_Grid_Layout
11.) REMEMBER WAYS TO SHOW COLOR (NAME,HEXA,DECIMAL,HSL) --use hsl..also use opacity to mix color..
12.) IF YOUR GIVEN Font is not on users computer-it will load default font "Times New Roman"--DO NOT include more than 2 or 3 fonts
13.)Font use-sans serif--https://s3.amazonaws.com/codecademy-content/courses/web-101/htmlcss1-diagram__fontanatomy.svg
14.)typeface(font-family), style(font-style:italic), weight(font-weight:bold|700), letter-spacing,word-spacing,text-transform,text-align,line-height..also know how to link google fonts -- (direct and using @font-face)

Read from here------>
bOX--
* ALWAYS START OR REMEBER BOX MODEL -every element is inside a box-- (width,height,padding,border,margin,overflow) (https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-4/diagram-boxmodel.svg)
**know the limitations of box model n also how to reset this--as it adds padding border size to overall size-- https://s3.amazonaws.com/codecademy-content/courses/web-101/htmlcss1-diagram__contentbox.svg
** to reset box model not to keep adding padding ,border on top of given width and height--reset it as below
* {
  box-sizing: border-box;
}
//browser default is box-sizing:content-box;
Css display and positions---->
kNOW what poistion (REALTIVE,FIXED,ABSOLUTE,STATIC-these are top level apply to divs usually) works better with display( inline,block,inline-block--these apply to elements usually like map,a,ul,table) and when to appl
** note that top,botton,right,left offset work in hadn with poistion elments.
** note that inline wont allow height and width.
** remebr certain elments like images,maps,a, are inline elments--meaning u cant set width and height ---SO YOU NEVER SET 'display:inline' for anything (see here for list of elments-https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements)
**remmeber tables, and many more are blockelments- https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements
**MOST IMP--IF YOU NEED TO SHOW DIVS NEXT TO EACH OTHER OR NAV LINKS horizontal---u need to rely on inline-block by setting items width and height..
**lets say you wan to show image on left and text on right u can use inline-block or use float to move text leftand right along with clear to tell how collapsing looks when these 2 collapse..(--USE CSS GRIDS -ITS MUCH EASIER--)

---
*for buttons on hover to changte color use transition or write css code for as .button:hover{} //.css class with action
*flow of elements in HTML. - A browser will render the elements of an HTML document that has no CSS from left to right, top to bottom, in the same order as they exist in the document.
*flow of elments can be controled using - (position,display,z-index,float,clear) //In addition to the properties that it provides to style HTML elements, CSS includes properties that change how a browser positions elements.

*Include space after : in styles
* Overiding rules (leaving !Important here) - ID style will overide  class and tag styles. //But dont use it often -Css claases are ment to be reused-meaning write individual classes and apply them where needed. Example- For instance, imagine a page with two headlines. One headline needs to be bold and blue, and the other needs to be bold and green. Instead of writing separate CSS rules for each headline that repeat each other’s code, it’s better to write a .bold CSS rule, a .green CSS rule, and a .blue CSS rule. Then you can give one headline the bold green classes, and the other the bold blue classes.
*order of priority is - id,class,tags
* to selected nested elments like a h5 tag inside a div tag which has id or class you can do say by saying --.classname h5 {} or #id h5 {}
* never use !important -
* use multi selector --so if you need to apply color blue in many places then say h1,p {color: blue}
* CSS can change background of elment-- One option is to make the background of an element an image. This is done through the CSS property background-image. Its syntax looks like this: .main-banner {
  background-image: url("https://www.example.com/image.jpg");
}
* to add a line use css -- like <div class="line"> </div> and in css define it like .line {}
Ways to include css styles into html - 

*to apply font style to entire body--set styles at body{font-family:red}
* if you need to add space between elments on top,left,right,bottom -use padding(space insid eof box ) or margin(space outside of box model) -refer to box model --dont forget margin collapse rules https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-4/diagram-verticalmargins.svg(top and bottom--browser selects larget--right and left-gets added )
* to put text in center use margin from box model (NOT THIS CENTER AT TOP CENTER--NOT LIKE PUTTING THING IN EXACT MIDDLE OF BOX) --make sure u add width 
* reset default browser styles -- using below thign in css  (All major web browsers have a default stylesheet they use in the absence of an external stylesheet. These default stylesheets are known as user agent stylesheets. In this case, the term “user agent“ is a technical term for the browser.)
 * {
  margin: 0;
  padding: 0;
}
* remember not use px as it stays the same on mobile --use  as percentages (%), ems and rems. CSS Grid introduced a new relative sizing unit — fr, like fraction.
-------------------------------------
1.) Inline Styling :  
Example-
<p style="color: red;">I'm learning to code!</p>;
<p style="color: red; font-size: 20px;">I'm learning to code!</p>

2.)Style Tag: Used to style multiple elements. Like multiple p or h1 tags. We add this inside HTML  head section.
<head>
  <style>
  p{ color:red;
     font-family: Arial
	 }

  </style>
</head>

3.) .Css files - create a new .css file and add your styles there. Import that into html HEAD section
<link href="https://www.codecademy.com/stylesheets/style.css" type="text/css" rel="stylesheet">
You can use the <link> element to link HTML and CSS files together. The <link> element must be placed within the head of the HTML file. It is a self-closing tag and requires the following three attributes:
href — like the anchor element, the value of this attribute must be the address, or path, to the CSS file.
type — this attribute describes the type of document that you are linking to (in this case, a CSS file). The value of this attribute should be set to text/css.
rel — this attribute describes the relationship between the HTML file and the CSS file. Because you are linking to a stylesheet, the value should be set to stylesheet.



Ways to style HTML elements-
-----------------------------]

1.) Tag Name - For example, in HTML, the tag for a paragraph element is <p>. The CSS syntax for selecting <p> elements is:
p {
color: blue;
}

2. Class Name :-CSS is not limited to selecting elements by tag name. HTML elements can have more than just a tag name; they can also have attributes. One common attribute is the class attribute. It’s also possible to select an element by its class attribute.
CSS classes are meant to be reused over many elements. By writing CSS classes, you can style elements in a variety of ways by mixing classes on HTML elements.

Example-
in html code
<p class="personal-details"> info....</p>

in css file
.personal-details {
color: yellow;
}

2.1) You can have multiple classes:-
<p class="one two"> info</p>

in csas file
.one{
color: yellow;
}
.two{
font-family: Arial:
}

3.) ID- If an HTML element needs to be styled uniquely 
While classes are meant to be used many times, an ID is meant to style only one element.
(no matter what classes are applied to the element), we can add an ID to the element. To add an ID to an element, the element needs an id attribute:
<p id="info">infooop....</p>

in .css file
#info{
color: green;
}

	

PARENT-CHILD CSS ELMENT SELECTION---
------------------------------

1.)chaining selectors

Example-
h1.special {

}
The code above would select only the h1 elements that have a class of special. If a p element also had a class of special, the rule in the example would not style the paragraph.


2.)Nested Elements
<ul class='main-list'>
  <li> ... </li>
  <li> ... </li>
  <li> ... </li>
</ul>

IN CSS STYLE File-

** ul li { } //styles all-we only want above html class element so,
 ** .main-list li {} //styles only above item not all 
------------------------------

3.) !important -overides everything
There is one thing that is even more specific than IDs: !important. !important can be applied to specific attributes instead of full rules. It will override any style no matter how specific it is. As a result, it should almost never be used. Once !important is used, it is very hard to override.

h5{
  color: rebeccapurple !important;
}


4.) multiple selectors - 
insted of writing same style like color for twice--do like belwo -
h1, 
.menu {
  font-family: Georgia;
}


-------------------------------------------------------  ---------------------------------------------------------------------------------------------------------------------------------------------------------------- 

BOX MODEL-


-----------------
Most used style elemtns :-
*color: maroon|teal;|rebeccapurple|SeaGreen|CornflowerBlue  //to color a text foreground
*background-color //to color background  // this property styles an element’s background color
*text-transform: uppercase|; //change to upper case

--------TEXT|FONT STYLES----
*font-family: cursive|Arial|Garamond|Courier New|Helvetica; (applied to h1,h2,h3,h4,h5,h6,p) (All fonts - https://www.cssfontstack.com/)
* font-family: "Garamond", "Times", serif; //use 'gramond' font for all. if garamong isnot there use "times" -if both are not there use 'serif-font' isntalled on user machine,.

*font-style:italic|normal
*font-weight: bold|normal|400|700|300 (400-default,700:bold,300:light); (applied to h1,h2,h3,h4,h5,h6,p) 
*word-spacing: 0.3em; //You can also increase the spacing between words in a body of text, technically known as word spacing.
*letter-spacing: 0.3em; //increasing the spacing between individual letters.
*text-transform: uppercase;
*text-align:right|left|center
*line-height:1.2|12PX --> A unitless number, such as 1.2. This number is an absolute value that will compute the line height as a ratio of the font size.
*text-align: right | left | center ;(applied to h1,h2,h3,h4,h5,h6,p.div--lets say u have content to show in center) 
 **Know aht serif and sans-serif is -
   *Serif - https://s3.amazonaws.com/codecademy-content/courses/web-101/htmlcss1-diagram__fontanatomy.svg

You can link fonts from 'Googlr Fonts'  https://fonts.google.com/ - in 2 ways
1.) Way 1- link directlyyou
you can download multiple fonts and link them --https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-6/video-fonts/Google+Fonts+2.mov
adding fonts-
<head>
  <link href="https://fonts.googleapis.com/css?family=Droid+Serif:400,700,700i|Playfair+Display:400,700,900i" rel="stylesheet">
</head>

2.)download and use @front-face --check this https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-6/video-fonts/latin-fonts.mov
example-
@font-face {
  font-family: 'Space Mono';
  font-style: normal;
  font-weight: 700;
  src: local('Space Mono Bold'), local('SpaceMono-Bold'), url(https://fonts.gstatic.com/s/spacemono/v1/vdpMRWfyjfCvDYTz00NEPGaVI6zN22yiurzcBKxPjFE.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2212, U+2215;
}

copy froma  different place-
@font-face {
  font-family: "Roboto";
  src: url(fonts/Roboto.woff2) format('woff2'),
       url(fonts/Roboto.woff) format('woff'),
       url(fonts/Roboto.tff) format('truetype');
}
--------------------------FONT EDN-----

*opacity: 0.5; Opacity can be used to make elements fade into others for a nice overlay effect. To adjust the opacity of an element, the syntax looks like this: (applied to DIV or images,classes  or h1-h6 or anything --like a div which has text)
*background-image: url("https://www.example.com/image.jpg"); // lets say you need to show an image in a page...u can do it via html or css..in css --first in html ass a div like <div class="image"> now in css define it like .image {bakground-image: url();}
*list-style: square; // used to change li or ul items roudneed icon to square 
---------------------------------------------------------------------
**BOX MODEL--content, borders, and padding(top,left,right,center),margin(used to center align text andmany more--values to set --top,left,right,bottom,collapse,min-width-height,max-width-height) (As you have seen, padding is space added inside an element’s border, while margin is space added outside an element’s border. ) -can be applied to anything form h1 to div and p etc, overflow ( hidden,scroll,visible)
------------------------------------ 
 *height:100px;(set to div or image )
  *width:200px (set to div or image )
  *border:A border is a line that surrounds an element, like a frame around a painting. Borders can be set with a specific width, style, and color. width:thin,medium,think ,style- 10 styles(https://developer.mozilla.org/en-US/docs/Web/CSS/border-style#Values) ,color:140 colors (https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)
     ** default border style is 'medium none color'		//where color is the current color of the element.  If width, style, or color are not set in the CSS file, the web browser assigns the default value for that property.
  *border-radius -- to smoothen corners or change to rounded border  //  border-radius: 5px; //  border-radius: 100%;//set to circle // can be applied to anything like image,bacground,div,p
  *padding- space between picture and fram--ie content and frame //  padding: 10px; you can also use padding-top,padding-bottom,padding-right,padding-left
  *  padding:20px 30px; //top and bottom to 20 and left an right to 30
  *  padding: 6px 11px 4px 9px; // 6 top,11 right, 4 botton, 9 left
  * margin- space from outside border line of a box -- //while padding is between inner content and box line//margin is from box line to outside-
    **margin: 20px; //have 20px space outside of box -on all 4 sides
	** margin-top /margin-bottom, margin-left,margin-right
	**  margin: 6px 10px 5px 12px; // top,right,bottom,left
	**   margin: 6px 12px; // 6-top and bottom ,12 -right and left
	** to put something at center use  --note width is must  -   div{width:100px, margin: 0 auto;}
	** margin collapse-- top and bottom -called vertical margins --browser will choose the tallest or highest margin --wheras for left and right it will add  them both (https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-4/diagram-verticalmargins.svg)
	**   min-width: 300px; // this property ensures a minimum width of an element’s box. //Because a web page can be viewed through displays of differing screen size, the content on the web page can suffer from those changes in size. To avoid this problem, CSS offers two properties that can limit how narrow or how wide an element’s box can be sized to.
	**   max-width: 600px; // this property ensures a maximum width of an element’s box.
	**   min-height: 150px; // this property ensures a minimum height for an element’s box.
	**     max-height: 300px; // this property ensures a maximum height of an element’s box.
  *overflow:hidden|scroll| visible (The total dimensions (364px by 244px) are calculated by adding all of the vertical dimensions together and all of the horizontal dimensions together. Sometimes, these components result in an element that is larger than the parent’s containing area.)
  *visibility:hidden | visible  (to show or not show something)
----------------------------
*CSS DISPLAY AND POSITIONING
------------------------------
 * position - used to position something to right,left,center,top,bottom etc...can be applied to div classes or anything that needs to be seperate from normal flow.
    ** position:static (default)
    ** position:relative(relative to parent or whatever is before you) -Meaning stand in lin relative to person in front of you-- 
      ** when setting relativ you need to tell top,bottom,left,right values -so browse will know realtive to parent at which location on page 
	  .box-bottom {background-color: DeepSkyBlue;position: relative;top: 20px;left: 50px;}
    ** position:absolute(i dont care about others --i will stand where ever i want -i dont follow the person front or any other in line-The element will be positioned relative to its closest positioned parent element) 
      .box-bottom {background-color: DeepSkyBlue;position: absolute;top: 20px;left: 50px;}
    ** position:Fixed(i follow the person infront of me --but i will not move when he moves--i am fixed at the position  care about others --fixed elments dont scroll wheras as absolute elments do--used for headers)
      .box-bottom {background-color: DeepSkyBlue;position: fixed;top: 20px;left: 50px;}
    --setting top:10px --tells browser to push it 10px down from its default poistion--not wrt to its parent.
 *z-index -  depth of element --you can saw who is 1st in line,2nd in line etc...only thing is if a person position  static (( default ))--we cant apply z-index--as he doesnt listen to anyone.
     ** start at 1 and goes to whatever we want--the component with hughest number is show on top of html page first--
 *display - used to tell if elment share horizontal space with other elemnts..
    **display:inline - (cant use height and width--but can use padding)this is default for <em>,<strong><a> --meaning they dont take extra space and fits in the content they need to like --example: i "em text here" go (list of inline elment- https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements) --you can set display:inline --so that no one can change its height and width.
	**display:block - (these elment take entire width by default--but u can chnge it-u can set height too--but note--u need to code it wrt to realtive poisition of others)some elments cant be show in same line like paragrpah,div,h1 to h6,tableas they exapns based on content --these are block elments- see this for other elments (https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements)
	**display:inline-block - (combines inline and block--show elements next to each other..and can take height and width -As an example a,b,c --we want them in a line with width and height-use this to show menu items or images next to each other--can be applied to divs or li items) - Images are the best example of default inline-block elements.	
 *float - if you dont want to use position to move anything right or left them use float --simply tyell float:left,float:right
 *clear - The float property can also be used to float multiple elements at once. However, when multiple floated elements have different heights, it can affect their layout on the page. Specifically, elements can “bump” into each other and not allow other elements to properly move to the left or right.
    ** claer:;eft|right|both|none (left — the left side of the element will not touch any other element within the same containing element.,both — neither side of the element will touch any other element within the same containing element.,none — the element can touch either side.)
----------------------------
*CSS GRIDS - THIS IS BEST WHEN COMPARED TO POSITION,BOX AND DISPLAY FOR DESIGING HTML PAGES
------------------------------
Example One-
.grid {
  display: grid;
  border: 2px blue solid;
  width: 400px;
  height: 500px;
  grid-template: repeat(3, 1fr) / 3fr 50% 1fr;
}



Example Two-

Step1 ->  here grid width is fixed--we dont wanna use this oftem --as we can tuse minmax for rows and columns
default property for any grid tos tart with:
height:500px;
width:100px:
**above 2 are used by below grid propertites--

or---use below---
Step1 -> variable grid width --u can use minmax size for rows/columns that way they can shrink or grow depending on size of content in it.
default property for any grid tos tart with:
height:500px;
**above 1 are used by below grid propertites--


or---use below---
Step1 ->here u remove 'height' because if a grid has extra rows comming in dynamically then i dont want the rows to overflow--instead i tell the grid to exapnd to showmore--see we also removed width --this way we can use minmax to shrink and grow
body {
  display: grid;
  grid: repeat(2, 100px) / repeat(2, 150px); 
  grid-auto-rows: 50px;
}


Step2 -> Use these to define more  (you can use grid-template-columns and grodi-template-rows or combine them into one using grid-template- and use repeat, fr,minmax to create rows easily)
grids properties-->
@@@@@@@@@To define columns ->
*  grid-template-columns:100px 50% 200px; //showing 3 columns //50% of width 100px given above--
*  grid-template-columns: repeat(3, 100px); //create 3 columns with size 100px
*  grid-template-columns: repeat(3, 1fr ); //create 3 columns with equal size.
*  grid-template-columns: repeat(2, 20px 50px ); //create 2 columns with sizes of 20px for first and 50px for second..
*  grid-template-columns: 100px minmax(100px, 500px) 100px; // first and 3rd colum sizes are fixed.. where as middle one varies between 100px and 500px depending on size of data in it **YOU NEED TO DELETE GRID WIDTH FOR THIS TO WORK

@@@@@@@@@@@@@@To define Rows ->
*  grid-template-rows: 10% 20% 600px; //shows 3 rows  --10% of 500px height given above..
*  grid-template-rows: repeat(3,1fr);
*  grid-template-columns: repeat(2, 20px 50px ); //create 2 columns with sizes of 20px for first and 50px for second..
*  grid-template-row: 100px minmax(100px, 500px) 100px; // first and 3rd row sizes are fixed.. where as middle one varies between 100px and 500px depending on size of data in it
*  grid-template-rows:5% 30% 10% repeat(3,10%) repeat(2,10%) 5%; //splitting 3rd row into 3 parts ..

@@@@@@@@@@@@@@@@@@@To combine both rows and colums ->
*  grid-template: 200px 300px / 20% 10% 70%; - can replace both column and rows as above into one -  //before slash is size of row ...here we have 2 rows and 3 columns
*  grid-template: 2fr 1fr 1fr / 1fr 3fr 1fr; //here we are telling there are 3 rows '2fr 1fr 1fr' and first row is twice the size of other two --see 2 fraction 
*  grid-template: 40% 50% 50px / 3fr 50% 1fr; //3 time the first column and 2nd column at 50% space of width and last column just 1 fraction
*  grid-template: 1fr 1fr 1fr / 3fr 50% 1fr; //rows taking equal height
*  grid-template: repeat(3, 1fr) / 3fr 50% 1fr;
*  grid-template: repeat(3, 1fr) / 3fr minmax(50px,300px) 1fr; //min max tells to resize column --make sure u dont have width



@@@@@@@@@@@@@@To show spaces between grid elemnts like rows and columns -> //note that grid gap wont add spaces at the begiging or end of grid--only in middle
grid-column-gap: 10px; 
grid-row-gap: 20px; 
grid-gap: 20px 10px; //set gap between rows as 20px and columns as 10px;
margin-bottom: -20px //to remove space
margin-top: -20px //to remove space

@@@@@@@@@@@@@@@@@To club or mix grids rows and columns -> VV IMP--HERE WE APPLY STYLES TO ITEMS THAT ARE INSIDE GRID--NOT TO ROWS OR COLUMNS*
ROWS-->
*Row grid lines and column grid lines start at 1 and end at a value that is 1 greater than the number of rows or columns the grid has. For example, if a grid has 5 rows, the grid row lines range from 1 to 6. If a grid has 8 rows, the grid row lines range from 1 to 9.
https://developer.mozilla.org/en-US/docs/Web/CSS/grid-row-start
eXAMPLE-> In this example, the HTML element of class item will take up two rows in the grid, rows 1 and 2. The values that grid-row-start and grid-row-end accept are grid lines.
.item {
  grid-row-start: 1;
  grid-row-end: 3;
}

or

.a {
  grid-row: 1 / 3;

}
cOLUMNS-> SAME AS ABOVE
.item {
  grid-column: 4 / span 2; // take 2 columns starting at 4
    grid-column: 2 / span 6; // take 6 columns starting at 2
}

or

.item {
  grid-column-start: 4;
  grid-column-end: span 2;
}

.item {
  grid-column-start: span 2;
  grid-column-end: 6;
}


@ Grid-area --> Combines row and column merging into one-
  .item {
  grid-area: 2 / 3 / 4 / span 5;
}

details--
grid-area takes four values separated by slashes. The order is important! This is how grid-area will interpret those values.

grid-row-start
grid-column-start
grid-row-end
grid-column-end


@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ grid-template-area
*** Instead of using rows and columns and dealing with numbers --why not use names ? that is what grid-tempalte-area does->
eXAMPLE-> // HERE WE ARE TELLLING there are 4 rows with 2 columns each --simple
 grid-template-areas: "head head"
                       "nav nav" 
                       "info services"
                       "footer footer";
now we define size of it--
  grid-template-rows: 300px 120px 800px 120px;
  grid-template-columns: 1fr 3fr; 


if we need to use them we just appply them using grid-area to individual dics in html--below tells header div to  take full row
  header {
  grid-area: head;
} 

below tells info and service to split like left and right--
.info {
  grid-area: info;
} 

.services {
  grid-area: services;
}
   



@@@@ grid-area

to tell how many rows/col a div spans--used in individual div---we can also use this show items on top of each others..like show text on top of image...
just set the image grid-area to needed col/rows and it will show on top....simple.... you can set z-index if needed


Extra properties for grid elmentts  --same like grid-area::
--->To move items or grid from LEFT TO RIGHT --use @justofy-items and justify-content --this apply to parent grid --meaning it is a overall setting--u cant use this to define individual items--
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@   MOVE ITEMS inside grid --LEFT TO RIGHT --use--  justify-items:(start:end:center:stretch:) --use this in parent class where u defeine grid--only--cat use it at individual grid item
check below to know all of them
https://developer.mozilla.org/en-US/docs/Web/CSS/justify-items#Values
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@  MOVE ENTIRE GRID FROM LEFT TO RIGHT =---use--justify-content-    this uses  width given to overall div/grid and puts grid in center,left,right,space-around etc..
check below -> https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content#Values 

--->To move items or grid from top  TO bottom  --use @align-items and align-content --this apply to parent grid --meaning it is a overall setting--u cant use this to define individual items--
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ aligh-items :(start|end|stretch|center))
https://developer.mozilla.org/en-US/docs/Web/CSS/justify-items#Values
@@@ align-content : moev entire grid from top-bottom 
check below-- https://developer.mozilla.org/en-US/docs/Web/CSS/align-content#Values
 
 
 -----> noww if a grid item wants to overide above 2 values it can use 'justify-self' for left to right alignemnt and 'align-self:(start|end|center|stretch)' for left-right alignment... this applies to indiviual div elemnts
  read more-- > https://developer.mozilla.org/en-US/docs/Web/CSS/align-self#Values
  
  
--> lets say if grid has rows that come dynamically--we can show them using below --
  
  SS Grid provides two properties to specify the size of grid tracks added implicitly: grid-auto-rows and grid-auto-columns.

grid-auto-rows specifies the height of implicitly added grid rows. grid-auto-columns specifies the width of implicitly added grid columns.

grid-auto-rows and grid-auto-columns accept the same values as their explicit counterparts, grid-template-rows and grid-template-columns:

pixels (px)
percentages (%)
fractions (fr)
the repeat() function


Example-->
body {
  display: grid;
  grid: repeat(2, 100px) / repeat(2, 150px); 
  grid-auto-rows: 50px;
}

 -->grid-auto-flow--> In addition to setting the dimensions of implicitly-added rows and columns, we can specify the order in which they are rendered. grid-auto-flow specifies whether new elements should be added to rows or columns.
grid-auto-flow:row|column|dense (row-add to row,column-add to column,dense - his keyword invokes an algorithm that attempts to fill holes earlier in the grid layout if smaller elements are added)  
example- grid-auto-flow: row dense; (you can pair them)


-------------------------------------------------------------------COLOR--------------------------------------
Color is of 2 types-- back and front ---it can set in below ways
color:red;  (string)(only 147 named colors)
color:  #8B4513; (hex)These are divided into 3 colors ->red,blue,green and each 2 letters is a hex decimal reprsenations of those colors.. (hexa is from 0-16) (https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)
color: rgb(23, 45, 23); (decimal) (16 lakh colors)(showing red,green and blue) - Here, each of the three values represents a color component, and each can have a decimal number value from 0 to 255 (so total 256 * 256 * 256 = 16,77,216 color possibilites)
color: hsl(120, 60%, 70%); // (hue,saturation lightness -hsl) (https://s3.amazonaws.com/codecademy-content/courses/learn-css-color/color_wheel_4_background.svg)
 *Hue - angle on color weel 0:red,120:green,240:blue,360:red
 *Saturation: intencity or purity of color ..goes from center of weel to top or end..
 *lightness - how light or dark is color --50% normal lightness ,100% light :0% darker-makes it closer to block
Opacity- color: hsla(34, 100%, 50%, 0.1); // Alpha is a decimal number from zero to one. If alpha is zero, the color will be completely transparent. If alpha is one, the color will be opaque. The value for half transparent would be 0.5.
  * mixing back and forth colors..like backgrounda nd foregorund..
  * can only be used with HSL and RGB
  
  
  -------------------------------------------------------------------TYPHOGRPAHY--------------------------------------
Color is of 2 types-- back and front ---it can set in below ways
color:red;  (string)(only 147 named colors)
color:  #8B4513; (hex)These are divided into 3 colors ->red,blue,green and each 2 letters is a hex decimal reprsenations of those colors.. (hexa is from 0-16) (https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)
color: rgb(23, 45, 23); (decimal) (16 lakh colors)(showing red,green and blue) - Here, each of the three values represents a color component, and each can have a decimal number value from 0 to 255 (so total 256 * 256 * 256 = 16,77,216 color possibilites)
color: hsl(120, 60%, 70%); // (hue,saturation lightness -hsl) (https://s3.amazonaws.com/codecademy-content/courses/learn-css-color/color_wheel_4_background.svg)
 *Hue - angle on color weel 0:red,120:green,240:blue,360:red
 *Saturation: intencity or purity of color ..goes from center of weel to top or end..
 *lightness - how light or dark is color --50% normal lightness ,100% light :0% darker-makes it closer to block
Opacity- color: hsla(34, 100%, 50%, 0.1); // Alpha is a decimal number from zero to one. If alpha is zero, the color will be completely transparent. If alpha is one, the color will be opaque. The value for half transparent would be 0.5.
  * mixing back and forth colors..like backgrounda nd foregorund..
  * can only be used with HSL and RGB
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------- DONE---------------------




--->now lets see below
-note- Note: CSS Grid is supported in the most recent versions of many browsers, but it is not supported universally. To make sure that you can get the most out of this course, check your browser version and see if it supports CSS Grid. If CSS Grid is not supported in your browser, you should switch or update to a supported browser and version.
https://www.whatsmybrowser.org/
https://caniuse.com/#feat=css-grid

Step1--> -How to create a grid  and rows ? To turn an HTML element into a grid container, you must set the element’s display property to grid (for a block-level grid) or inline-grid (for an inline grid). Then, you can assign other properties to lay out the grid.
in html-
  <div class="grid">
    <div class="box a">A</div>
    <div class="box b">B</div>
  </div>
 In css-
 .grid {
  border: 2px blue solid;
  width: 400px;
  height: 500px;
  display:grid;
}

.box {
  background-color: beige;
  color: black;
  border-radius: 5px;
  border: 2px dodgerblue solid;
}

Step2 ---> How to create columns -- by default grid has only one..we can use '*grid-template-columns'

Example- css with 2 columns --one at 100px an another at 200px->
.grid {
  display: grid;
  width: 500px;
  grid-template-columns: 100px 200px;
}

or
.grid {
  display: grid;
  width: 1000px;
  grid-template-columns: 20% 50%;
}

Step 3 --> Creating rows - use grid-template-columns
.grid {
  display: grid;
  width: 1000px;
  height: 500px;
  grid-template-columns: 100px 200px;
  grid-template-rows: 10% 20% 600px;
}


Step 3  == Step 1 & 2 mixed - (check above for more info -- on different values we can pass)The property grid-template can replace the previous two CSS properties. Both grid-template-rows and grid-template-columns are nowhere to be found in the following code!
example-
.grid {
  display: grid;
  width: 1000px;
  height: 500px;
  grid-template: 200px 300px / 20% 10% 70%;
}

before slash is size of row ...here we have 2 rows and 3 columns
