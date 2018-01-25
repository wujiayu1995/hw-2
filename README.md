<!DOCTYPE html>
<html lang="en">
<head>
<meta charset= "utf-8">
    <title>Rolling looping</title>
    
  <style type="text/css ">
    
      @import url('https://fonts.googleapis.com/css?family=Amatic+SC');
      @import url('https://fonts.googleapis.com/css?family=Amatic+SC|Coming+Soon');
      
      h1 {font-family: 'Amatic SC', cursive;
          font-size: 200%;}
      
      
      ul {list-style-type: none;
        margin: 50px;
        padding-left:30px;
        }
      
    body {
      font-family: sans-serif;
    text-align: center;}
    img {
      
      padding-left: 5cm;
    }
    .red {
      color: red;
    }
      
      body {padding: 5rem;}
      
      
  </style>
    
    
</head>
<body>
    
<header>  
    
  <h1>Whee!</h1>
   
    <nav>
    
    <ul>
        
      <li><a href="#" target ="_blank">Introduction</a></li>  
       <li><a href="#" target ="_blank">Address</a></li>   
        <li><a href="#" target ="_blank">Guide</a></li>  
        
    </ul>
    
    
    </nav>
    
    
</header>  

  <img id="roller" src="http://images.mentalfloss.com/sites/default/files/styles/width-constrained-728/public/503373-iStock-186293315.jpg" alt="roller coaster">

  <script type="text/javascript">
    // Description:

    // When complete, this program will ask the user how many roller coaster rides
    // they'd like to go on, then execute a block of code that many times.
    // The block will output which "ride" they're on, and change which image
    // is displayed on the page. The images shown will cycle through a list
    // of possible sources, though this happens so quickly that the user will only see
    // the final one shown.

    // There are explanatory comments thoughout. The work that still needs to be done
    // is noted in TODO comments. Please complete this work.


    // an array of possible image source values
      
      var experience = prompt ("Have you ever tried this before?")
      if( experience == "yes")
        {console. log ("me too!")}
      else if (experience == "no")
        {console. log ("You need a try!")}
      
      var imageSources = [
      "http://images.mentalfloss.com/sites/default/files/styles/width-constrained-728/public/503373-iStock-186293315.jpg",
      "https://media4.s-nbcnews.com/j/newscms/2017_31/1270023/wonder-woman-roller-coaster-today-inline-170803_7e4934000dfd84cdbb6b2f4900a03988.today-inline-large.jpg",
      "http://cdn.cnn.com/cnnnext/dam/assets/160520171710-07-stormchaser-jpg-best-coasters-super-169.jpg",
      "https://thediabeticjourney.com/wp-content/uploads/2016/08/diabetes-rollercoaster.png"
    ]

    // select the <img> tag with id of "roller" from the HTML
    var theImg = document.querySelector("img#roller");

    // set the src attribute of the img to be the first element in source array
   theImg.setAttribute("src", imageSources[0]);

    // TODO: set howMany variable to a value user inputs
    var howMany = prompt ("how many times?")
  
    var counter = 1
    // TODO: execute this loop the number of times user requested
    while(counter <= 100){
      console.log("Wheee! This is the ", counter+5, " time we've done this!");

      // find value of counter modulo length of sources array-
      // this value will increase by one on each iteration of the loop,
      // so image source will cycle through all possible images
      var theOne = counter % imageSources.length;
      // reset the src of the image to the next member of the sources array
      theImg.setAttribute("src", imageSources[theOne]);

      // TODO: increment the counter
    }

    // EXTRA CHALLENGES:
    // 1. Using JS, add a class of "red" to the <h1>.
    //    This only needs to be done once, so code should be outside loop.
    // 2. Execute the loop only half as many times, or twice as many times, as the user requested.
    // 3. Add a pause to each loop, so user can see each image as it cycles past.
    //    This is a difficult one!

  </script>   
    
</body>
</html>
