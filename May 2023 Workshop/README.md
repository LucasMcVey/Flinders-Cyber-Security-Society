Summary: In this guide we will be covering challenges: "Put an additional product into another user's shopping basket" and "Forge an essentially unsigned JWT token"

Challenge 1 - Put an additional product into another user's shopping basket

First step is to create an additional user account as shown in the picture below:
![](Screenshot%203.png)

Next step is to add any item to the basket:
![](Screenshot%204.png)

Go back to burpsuite and look for the POST method and the url of /api/BasketItems. Right click and send to repeater
![](Screenshot%208.png)

At the bottom of the request modify by including a second basket Id after the first Basket Id like in the image below:

![](Screenshot%209.png)
{"ProductId": 15,"BasketId": "6","quantity": 1,"BasketId": "1"}



Challenge 2 - Forge an essentially unsigned JWT token

First step is to look through burp suite for a get request that has the Authroization : Bearer text

![](Screenshot%2010.png)

Copy the first part before the "." and paste that into a website like Cyberchef and add the from base 64 module by dragging the operation onto the recipe area.


![](Screenshot%2011.png)
Copy the output and replace the input with it, change the HS256 to none.

Change the recipe from "From base 64" to "To base 64"

I recommend copying the base 64 output text into a notepad to keep track of it for later.

![](Screenshot%2016.png)

Go back to burpsuite and copy the text after the first dot but before the last dot as shown in the picture below:

![](Screenshot%2013.png)

Paste the text into the input part of cyber chef and change the recipe back to From base64

![](Screenshot%2014.png)

Copy the output and paste it into the input. After that change the recipe from "From base 64" to "to base 64". Modify the email to include jwtn3d@juice-sh.op like in the picture: 
![](Screenshot%2015.png)
I also suggest copying the output and put it into a notepad


You should have something like this:

![](Screenshot%2017.png)

Combine the first base64 string with the second base64 string and change the = sign to a "." like this picture
![](Screenshot%2018.png)