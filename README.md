INFORMATION FOR INDEX.HTML: 

The index.html file is used for making edits to the actual contents of the website. Within this file you can change the order in which items are displayed, where the items 
link to, and the type of content that is displayed. The site is defined as having a "head" section and a "body" section. The head contains the base information for the 
webpage and allows for you to define or reference information from other files that will be used throughout the code, in this case the styles.css which can be seen below. 

    <title>Audubon Society at UW-Madison</title> 
    <link rel="stylesheet" href="styles.css">

The body section contains the important links and images seen on the website which are organized by divisions seen as "div" in the code. Each division also has a class 
associated with it which relates to the styles.css file that will be explained later. Once the division and it's class type have been called you would then insert whatever 
content you like, however, different division classes are used for different types of content. This is best understood by playing with the href"" portions of the code to see how they affect the site. Some examples can be seen below of how the divisions and the classes work. 

    <div class="headerImageContainer">
          <img src="images/IMG_3825.png" alt="Audubon Society at UW-Madison Logo" class="headerImage">
    </div>
  
The "/div" call is used to tell the code when you are done inputting content into a division. The example shown above is for images, specifically the image displayed at the 
top of the site. The img src="" function searches github's images folder for any uploaded images you have called out. The alt would display a message when the image is 
unable to load. 

    <div class="headerText">
          <h1>Audubon Society at UW-Madison</h1>
    </div>
  
The above code uses "h1" to define the text as being the top priority heading which allows for the title to come first on the webpage. 
  
    <div class="linkContainer">
        <div>
                <a class="tree" href="#AboutUs">About Us</a>
        </div>
        <div>
                <a class="tree" href="https://docs.google.com/forms/d/e/1FAIpQLScRSfNG7DM2xQ63GiA_UVvONueKkiXw_Xubvo2D0RZG-soowA/viewform?usp=sf_link" target="_blank">Meeting Sign-In</a>
        </div>
        
The above code uses the "a" command which allows for items with a hyperlink to be created. These hyperlinks can either send you to another section of the site, as seen with 
the href="#AboutUs" call, or send you to another site entirely, such as with the Meeting Sign In item that is linked to an attendance google form. The target"" command allows you to initialize an object that the hyperlink attaches to so that the website does not display the actual link itself, so the site would display Meeting Sign In and when you click on this option it would take you to the linked google form. 

    <div class="bodyText">
        <p>
              We provide interested UW students and community members opportunities to engage in extracurricular dialogue, observation, and study of birds and bird conservation.br><br
              <strong>Our goal is to protect birds and the places they need to thrive.</strong><br><br>
              Interested in getting involved with ASUM? Send a message to <b>audubonsocietyuw@gmail.com</b> and check out <a href="https://win.wisc.edu/organization/asum" class="link" target="_blank">our WIN page.</a>
        </p>
    </div>
  
This example shows usage of the "p" command which creates a paragraph of text that allows you to nest other commands within it. This is seen with the "strong" command which 
allows for an entire line of text to be made bold, as well as the "b" command which makes a single item bold and the previously mentioned "a" command for creating hyperlinks.



INFORMATION FOR STYLES.CSS: 

This file connects to the content inputted to the index.html file through the "class" inputs. These classes relate to the cosmetics or appearance of the website, controlling the font, color, and shape of your content. Many of the functions in a .css file are flexible and can be modified to be as complex or as simple as you would like. There are many resources online that give great examples of how to generate a specific color or shape for your site. AI is often a very helpful tool in brainstorming ideas on how to give the site a certain look. 

    body {
      background: rgb(0, 0, 0);
      background: linear-gradient(
        0deg,
        #96A68E 0%,
        #455D3B 100%
      ); /*6b705c and a5a58d*/ 
      background-repeat: no-repeat;
      height: 100%;
      }

The example above shows some of the inputs used to control the color of the background of the site. Colors are defined either by "background" or "color" with the rgb() command input, which allows you to set a ratio of color values that combine to make one color, or by inputting a colors HEX code, in this case the HEX is acting as an input to the linear-gradient command shown by #96A68E and #455D3B. You can search up a color wheel to select a color and they will typically give you the associated HEX code. There are also base colors that can be inputted by typing in their name, i.e. white, black, red, etc. 

    .headerImageContainer {
      display: flex;
      align-content: center;
      justify-content: center;
      height: 200px;
    }

The above code shows the commands used to align the content in the center of the window and how the size of an object can be controlled. Dimensions for a website are defined by px which stands for pixel rather than a typical measurement like inches or centimeters. The website can be thought of as a grid of pixels, so the height of 200px means that the image will take up 200 pixels vertically within the grid. 

    .tree {
      display: flex;
      align-content: center;
      justify-content: center;
      border: 2px white solid;
        background-color: #8c3131;
      text-decoration: none;
      font-family: Verdana, Geneva, Tahoma, sans-serif;
      font-size: 1.5rem;
      color: rgb(235, 235, 235);
      margin: 30px;
      padding: 30px;
    }

This code contains the font-family command with a list input of fonts. Not every font is available to be used by the .html file type, thus the list input of fonts allows you to define multiple fonts that you like with the order in which they are put into the list being the priority they are given in the html file. This means that the html will first try to apply the font Verdana to the site, but if it is unable to due to the version type that the user has, then the code will attempt to apply the next font within the list to the site. The margin function is also shown here and is used to define the spacing between items neighboring any objects within the .tree class type, hencewhy the input has the px unit associated with it. 
