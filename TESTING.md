## Testing

_Code Validators_

All code passed validation tests from the [HTML](https://validator.w3.org/) and [CSS](https://jigsaw.w3.org/css-validator/) validation websites.

The python code passed the [PEP8](http://pep8online.com/) compliance test.

_Speed_

I used [GT Metrix](https://gtmetrix.com/) to analyse the speed of the website, which gave an overall grade of A.

_User Stories_

Intuitive:
 - The title of the site gives an idea of its purpose.
 - The homepage displays a suitable hero image, and overlaying headline explaining the site's purpose.
 - There are further details about the site included below the hero image/on the footer.

Presentation:
 - Used Materialize CSS to present in a clean grid format.
 - Simple colour scheme used with plenty of white spaces to keep things clean and not overwhelm user.

Searchable:
 - Clear search function at top of recipes page, enabling searching by recipe title/ingredients.

Easy login/signup:
 - Two simple pages for these functions, where only 2 inputs are required, and clear instructions displayed regarding the requirements for these inputs.

Add/edit recipe:
 - Buttons for these functions have been included for these functions on the profile page.
 - Add Recipe also appears on the navbar (once user is logged in).

_Features_

The following details how the various features of the site have been tested for their intended purpose.

GENERAL

 - Top navbar is fixed at the top for all pages
 - Navbar changes to burger icon on mobile
	- All navbar links redirect to correct site page
 - Footer appears at bottom of all pages
 	- Footer social links all open in new tabs

INDEX
 
 - Button titled RECIPES takes you to recipes page
 - Button titled REGISTER takes you to register page

RECIPES

 - Search:
	- Entering search terms in input area brings back appropriate reuslts (i.e. recipes where recipe/ingredients matches the search term)
	- If invalid search term entered "No results found!" message displayed
	- Clicking the "magnifying glass" icon activates the search and displays recipe cards matching search criteria
	- Clicking the "x" icon resets the search and displays all recipe cards again
 - Recipe Card:
	- Clicking on recipe card image takes you to the details page for that recipe
 	- Button titled RECIPES takes you back to recipes page

LOGIN

 - Entering correct username/password takes you to user profile page/displays "welcome, username" message
 - Entering incorrect username and/or password displays "Incorrect username and/or password" message 
 - Entering username/password matching required format highlights input line as green
 - Entering username/password not matching required format highlights input line as red and displays "Please match format requested" message
 - link
 - "Register account" link at bottom takes you to register page
 
REGISTER

 - Entering username/password in required format completes registration and takes you to user profile page/displays "Registration successful" message
 - Entering username/password not matching required format highlights input line as red and displays "Please match format requested" message

PROFILE

 - Profile page only displays recipe cards added by that user
 - Clicking on recipe card image takes you to the details page for that recipe
 - Add Recipe button at top of page takes you to add recipe page
 - Edit/Delete buttons appear at bottom of each recipe card
	- Edit button takes you edit recipe page, with form pre-filled with relevant recipe details
	- Delete button removes recipe from database
		- Hovering over Delete button displays "Make sure you want to delete" message

LOGGED IN NAVBAR
 - Menu items in navbar change when logged in to display: Profile/Add Recipe/Log Out
 	- Profile link takes you to user profile page
 	- Add Recipe link takes you to add recipe page
	- Log Out link takes you back to log in page and displays "You have been logged out" message

EDIT RECIPE
 - Form pre-filled with relevant recipe details
 - CANCEL button takes you back to recipes page
 - EDIT button edits recipe in database and displays "Recipe updated!" message

ADD RECIPE
 - Any form inputs not matching required format highlights input line as red
 - Attempting to click ADD RECIPE button with missing inputs displays "Please fill in this field" message
 - Clicking ADD RECIPE button when form filled correctly adds recipe to database/takes you to recipes page/displays "Recipe added!" messsage
 - The "serves/time/vegetarian" inputs are all displayed on the recipe details page within materialize chip elements
 	- The vegetarian chip element only appears when the vegetarian checkbox has been checked on the add/edit recipe form


_Responsiveness_
	
I tested the website by changing the screen size on my display, and using the inspect function on developer tools to show how it looks on different devices.

I tested the website on various browsers/devices which were available to me.


_Bugs_

The following details any issues I came across which are now resolved, for reference:

 - Displaying the recipe ingredients/method on seperate lines: to get each ingredient/step to display on a seperate line, I used splitlines in my jinja code, and prompted the user to enter each ingredient/step on the input form 
    - Searched on Slack and found this online [Javatpoint](https://www.javatpoint.com/how-to-split-a-string-in-java-with-delimiter#:~:text=In%20Java,%20splitting%20string%20is%20an%20important%20and,the%20split%20()%20method%20of%20the%20String%20class.)
 
 - Displaying individual recipe details: to call up individual recipe details on the recipe_details page, used find_one in the relevant section on app.py:
    - Searched on Slack, saw solution from [Igor Basuga](https://code-institute-room.slack.com/team/UPDFEU62U)
 
 - Displaying user recipes only on profile page: to display users recipes only, added if statement (if session.user|lower == recipe.recipe_addedby|lower) in jinja:
    - Used Code Institute Task Manger Mini-Project by [Tim Nelson](https://code-institute-room.slack.com/team/UBVE86CJC) as the basis and modified code for my intended purpose.
 
 - Displaying full-width hero image: wanted hero image on homepage to be full-width, found that Materialize CSS "container" class doesn't stretch to full width, so removed this class from the base template: 
    - Used dev tools to see "container" CSS properties 
    
 - Custom 404/500 error pages: didn't know how to action this, searched on Slack where someone had provided solution:
    - Searched on Slack, saw solution from [Heather Olcot](https://code-institute-room.slack.com/team/U9CBT421G) 
 
 - Improving loading time by adding lazy loading to images: 
    - Searced on Slack, read about this in a post from [Antonio Augello](https://code-institute-room.slack.com/team/UCS5Q5LKH)
    
The following details any issues which remain unresolved:

 - Forcing URL: at the moment it is possible to "force" the URL to add/edit/delete recipes into the browser:
	- if you aren't logged in you're not able add/edit recipes
	- if you are logged in you can edit someone else's recipe
	- you can delete a recipe even if not logged in/not your own recipe
	- as login functionality is not actually required for this project, and due to timing constraints, I have left this as a bug to be resolved in the future
 
 - Uploading image files:
	- adding a recipe involves inputting a URL, there is no option to upload a file
	- from searching on google/slack, I found adding this functionality is not straightforward
	- due to timing constraints, this has been left as a feature to be added in the future

 - Modal for confirming recipe deletion:
	- for the recipe delete button, it would be preferred to have a modal popup and ask the user to confirm their intention to delete for better defensive programming
	- due to timing constraints, I used a Materialize CSS tooltip instead to display a warning message instead, when hovering over the delete button

    