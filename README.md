## Milestone 3 – EasyDinner Website

I am designing a recipe sharing database website. The website will contain recipes for quick, easy family dinners.

[EasyDinner](https://ms3-easydinner.herokuapp.com/)

![picture](static/image/readme/responsive.PNG)

## Index

- <a href="#UX">UX</a>
    - <a href="#Overview">Overview</a>
    - <a href="#Stories">User Stories</a>
    - <a href="#5S">5 S's</a>
- <a href="#Features">Features</a>
    - <a href="#Existing">Existing</a>
    - <a href="#Left">Left to Implement</a>
- <a href="#Technologies">Technologies Used</a>
- <a href="#Testing">Testing</a>
- <a href="#Deployment">Deployment</a>
    - <a href="#MongoDB">MongoDB</a>
    - <a href="#GitHub">GitHub</a>
    - <a href="#Heroku">Heroku</a>
- <a href="#Credits">Credits</a>

<span id="UX"></span>

## UX

<span id="Overview"></span>

_Overview_

The aim of the project is to design a recipe website containing a database of quick, easy family meals. 
The website is designed to cater to those specifically looking for recipes which fit this criteria, for example busy parents who don't have time or energy to think about dinner, or prepare complicated meals for their family! 
As this website will contain an active database, there will be an option for users to signup to add their own recipes.
The website is designed to be suitable for use on all devices, from desktop to mobile. 

<span id="Stories"></span>

_User Stories_
	
   *	I want the website to be intuitive, so I can get an impression of what it does from first glance.
   *	I want the website to be visually appealing and well presented.
   *	I want the recipe listing feature to be searchable, so I can search for specific recipes I may be interested in.
   *	I want an easy way to login or signup to the website.
   *	I want it to be easy to add/edit a recipe.

<span id="5S"></span>

_5 S's_

**Strategy** 

The primary goal is to provide a searchable database of recipes for website users, which is visually appealing, and easy to use.

**Scope** 

The overall look and feel of the website was influenced by researching similar websites (credits at end):
-	These are simple/clean in design.
-	Recipes are displayed in a grid of "cards" consisting of an image and recipe title, clicking on a recipe card takes you to the recipe details page.
-	There is a facility to search recipes. 
-	There is a facility to login/register to the site, which then takes you to your profile page.

With this in mind, my website will include:
- 	A homepage with some details about the website, some featured recipes, and links to sign in or register (included to give an overview of the site, and make it intuitive for the user).
-	A searchable recipes page, which will display the recipes in a "card" or grid format.
-	Clicking on the recipe "card" will bring up that particular recipe's details page, including the ingredients/method.
-	A login/sign up page.
-	Once logged in, the user will be directed to their user profile page, which will give the user options to add/edit their own recipes.

**Structure** 

In line with the features identified in the scope section, the website will be structured as follows:

1.	Homepage:

	-	Navbar at top, showing website title/logo, and links to other pages (fixed/featured on all pages for familiarity/ease of use).
	-	Hero image with text explaining the purpose of the site.
	- 	Links to log in or sign in.
	-	Footer showing social media links (fixed/featured on all pages for familiarity/ease of use).
	- 	This page has been included/designed in this way to give the user an effective snapshot of the site, you can see all the main features of the site from looking at this page:
		-	Introductory text and hero image "explain" the sites purpose.
		-	The sign in/log in links show that this is a interactive/sharing site, the accompanying text will encourage the user to do so.
  
2.	Recipes:

	-	A search feature at the top of the page. 
	-	Recipes displayed via "cards" or thumbnails, consisting of the recipe image/recipe title, in a grid format.

3.	Recipe Details:
	
	-	Will include all recipe details including ingredients, method, added by, prep time, servings.

4. 	Login/Sign Up:
	-	The log in and sign up pages will be the same, requiring the user to input username/password.

5. 	Profile:
	-	Will include the facility to add users own recipes, as well as edit any recipes already submitted.

**Skeleton** 

[Wireframes - includes sitemap and database schema](https://github.com/upeshp/MS3_EasyDinner/tree/master/assets/docs/wireframe)

**Surface** 

-	The colour scheme will be influenced from the research detailed in the scope section above.
-	The websites tend to use simple colour schemes, with green/teal often being used.
-	Green is associated with being peaceful and healthy, which is perfect for this site, so this colour will be used in my site for any main features. [Source: CrazyEgg](https://www.crazyegg.com/blog/website-color-palettes/)
-	A clear, easy to read, friendly style of font was wanted, I decided on a combination of Open Sans/Roboto (Google Fonts) as I thought these fonts meet these particular requirements.

<span id="Features"></span>

## Features

<span id="Existing"></span>

_Existing_

The website uses Materialize CSS features:

-   Navbar (top navbar)
-	Sidenav (to turn into sidenav on mobile)
- 	Cards (to display recipes)
-   Forms (to add/edit recipes)
- 	Buttons (for links to other pages and add/edit/delete actions)
- 	Footer (bottom footer)
-   Tooltip (to display message on delete button)
-   Chips (to display some recipe info)

In addition the following features are used:

-   Site linked to MongoDB database
-   Search facility to search recipes
-   Login/signup functionality to become a registered user
-   User profile page displaying users recipes only
-   Passwords are hashed so not shown on the database
-   Full CRUD functionality included
-   Custom 404/500 error pages

<span id="Left"></span>

_Left to Implement_

The following features were considered during the build of the site, however due to time constraints, these were not included in this version, but could be added at a later date:

- 	Ability to rate/mark a recipe as a favourite.
-	Introducing recipe categories e.g. vegetarian/quick/easy etc, which can then be filtered.
-	Pagination to ensure not too many recipes displayed on 1 page.
-   Displaying latest or featured recipes on homepage.
-   See unresolved bugs section in [Testing](https://github.com/upeshp/MS3_EasyDinner/blob/master/TESTING.md) for further features left to implement.

<span id="Technologies"></span>

## Technologies Used

Languages:
- 	HTML5
-	CSS3
-	Javascript
-	Python (incl. Jinja)

Database:
-   MongoDB

Frameworks:
-   Materialize CSS
-   Flask
-   Jquery

Storing/editing/deploying Code:
-	Gitpod
-	Github
-   Heroku

Other:
-   Google Fonts
-   Font Awesome

<span id="Testing"></span>

## Testing

Testing documentation can be found [here](https://github.com/upeshp/MS3_EasyDinner/blob/master/TESTING.md).

<span id="Deployment"></span>

## Deployment

The source code for this site is in GitHub. Heroku was used to deploy the site. MongoDB was used for the database.

<span id="MongoDB"></span>

_MongoDB_

The following collection was used for the recipes:

![mongodb](static/image/readme/mongodb.PNG)

<span id="GitHub"></span>

_GitHub_

To clone the code from GitHub:

1.	On GitHub, navigate to the main page of the repository.
2.	Above the list of files, click Code:

    ![view](static/image/readme/deployment_github.png)

3.	To clone the repository using HTTPS, click HTTPS under "Clone".
4.	Open Git Bash.
5.	Change the current working directory to the location where you want the cloned directory.
6.	Type git clone, and then paste the URL you copied earlier:
    ```$ git clone https://github.com/YOUR-USERNAME/MS3_EasyDinner.git```
7.	Press Enter to create your local clone.
8.  Create your own env.py file to store variables, and ensure this is listed in your .gitignore file to keep these from being displayed publicly:

     - Import os 
     - os.environ.setdefault("IP", "enter value") 
     - os.environ.setdefault("PORT", "enter value") 
     - os.environ.setdefault("SECRET_KEY", "enter value") 
     - os.environ.setdefault("MONGO_URI", "enter value") 
     - os.environ.setdefault("MONGO_DBNAME", "enter value")
 
<span id="Heroku"></span>

_Deployment to Heroku_

1.  Setup files which Heroku needs in your terminal:

    *requirements.txt*: tells Heroku which applications and dependencies are required to run our app.
    
    *Procfile*: what Heroku looks for to know which file runs the app (use capital P for Procfile, and delete blank line at bottom of Procfile as may cause problems when running on Heroku).
    
    ![setup files](static/image/readme/deployment1.png)

2.  Go to Heroku, once logged into your dashboard, click ‘Create new app’:

    ![new app](static/image/readme/deployment2a.png)
    
    Create app name (must be unique, and generally use a 'dash' or 'minus' instead of spaces, and all lowercase letters):
    
    ![app name](static/image/readme/deployment2b.png)
    
    Choose region closest to you:
    
    ![region](static/image/readme/deployment2c.png)
    
    Then click ‘Create app’:
    
    ![create app](static/image/readme/deployment2d.png)

3.	Setup automatic deployment from your GitHub repository:

    ![auto deploy](static/image/readme/deployment3a.png)
    
    Make sure your GitHub profile is displayed:
    
    ![profile](static/image/readme/deployment3b.png)
    
    Then add your repository name:
    
    ![repo name](static/image/readme/deployment3c.png)
    
    Click ‘Search’:
    
    ![search](static/image/readme/deployment3d.png)
    
    Once it finds your repo, click 'Connect' to connect to this app:
    
    ![connect](static/image/readme/deployment3e.png)

4.	Click on ‘Settings’:
    
    ![settings](static/image/readme/deployment4a.png)
    
    Then click ‘Reveal Config Vars’
    
    ![config](static/image/readme/deployment4b.png)
    
    Then enter the variables (from the env.py) file to securely tell Heroku which variables are required:
     - IP
     - PORT
     - MONGO_DBNAME
     - MONGO_URI
     - SECRET_KEY

5.	Push two new files (requirements.txt and Profile) to repository, in terminal, add/commit/push these:
    
    ![push](static/image/readme/deployment5.PNG)

6.	Back in Heroku, can now safely ‘Enable Automatic Deployment’:
    
    ![enable](static/image/readme/deployment6a.png)

    Then ‘Deploy Branch’:
    
    ![deploy](static/image/readme/deployment6b.png)

7.	That should take a minute to build, once it's done, you'll see ‘Your app was successfully deployed.’ Click ‘View’ to launch your new app:
    
    ![view](static/image/readme/deployment7.png)


<span id="Credits"></span>

## Credits

_Tutorials_

I used the Code Institute Task Manger Mini-Project by [Tim Nelson](https://code-institute-room.slack.com/team/UBVE86CJC) as the main basis of my own project.

_Slack Community_

I was able to resolve many issues encountered after searching on Slack in the Code Institute community, the following in particular have posted content which I found useful:

 - [Ed Bradley](https://code-institute-room.slack.com/team/U0112RF2N79)
 - [Igor Basuga](https://code-institute-room.slack.com/team/UPDFEU62U)
 - [Daniel Hayes](https://code-institute-room.slack.com/team/UCQ2AF9JT)
 - [Malia Havlicek](https://code-institute-room.slack.com/team/UERRFE54G)
 - [Heather Olcot](https://code-institute-room.slack.com/team/U9CBT421G)
 - [Antonio Augello](https://code-institute-room.slack.com/team/UCS5Q5LKH)

I would also like to thank the Slack peer-code-review community for reviewing my project.

_Student Projects_

 - [Self Isolution](https://github.com/Edb83/self-isolution)
 - [Wean Cuisine](https://github.com/Lucyjpjones/wean-cuisine)
 - [McTastic Recipes](https://github.com/Sean-Mc-Mahon/McTasticRecipes)

_Images_

Hero image on homepage from [Pixabay](https://pixabay.com/).

Recipe images from [Hello Fresh](https://www.hellofresh.co.uk/recipes/quick-recipes).

(Website created for educational purposes only, not intended to be used for commercial purposes)

_Mentor_

Code Institute mentor Akshat Garg.
 
_Research_

I used the following websites as a reference in the design process:

 - [Hello Fresh](https://www.hellofresh.co.uk/recipes/quick-recipes)
 - [Delicious Magazine](https://www.deliciousmagazine.co.uk/collections/healthy-family-meals/)