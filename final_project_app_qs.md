# SI 364 - Final Project questions

## Overall

* **What's a one-two sentence description of what your app will do?**
My app will be an interactive game app based around one or many users guessing the name of a song or artist based on a small sample of lyrics from a song. 

## The Data

* **What data will your app use? From where will you get it? (e.g. scraping a site? what site? -- careful not to run it too much. An API? Which API?)**

My app will get data from the Musixmatch api and the Itunes api

* **What data will a user need to enter into a form?**
The user will choose what genre, or artist to play for the game 

* **How many fields will your form have? What's an example of some data user might enter into it?**
My fields will require a users name, how many players will be playing, and the type of game they would want to play (guessing song titles based on the collection of an artist or a genre)

* **After a user enters data into the form, what happens? Does that data help a user search for more data? Does that data get saved in a database? Does that determine what already-saved data the user should see?**
The app will make requests to the api to generate a random sample of lyrics, and the player will have to make their best attempt at guessing the song

* **What models will you have in your application?**
I will have a leaderboard model, a player model, and a game model

* **What fields will each model have?**
the leaderboard model will have the name and score of the each player after they have finished their game. The game model will keep track of game statistics such as how many players their are, what are their names, how many points they have, and how many lives they have left. The player model will have fields such as name and high score.

* **What uniqueness constraints will there be on each table? (e.g. can't add a song with the same title as an existing song)**
You will not be able to make two players in the same game that have the same name, the leaderboard will not be able to have repeated scores for the same player, and only one player can have one name

* **What relationships will exist between the tables? What's a 1:many relationship between? What about a many:many relationship?**
There is a one to many relationship between a game and multiple players, and there is a many to many relationship between the scores on the leaderboards and the players.

* **How many get_or_create functions will you need? In what order will you invoke them? Which one will need to invoke at least one of the others?**
I will need a get_or_create function for the game and for the players. the game will be created before the players are created, and the get_or_create game function will get or create players.

## The Pages

* **How many pages (routes) will your application have?**
6

* **How many different views will a user be able to see, NOT counting errors?**
4

* **Basically, what will a user see on each page / at each route? Will it change depending on something else -- e.g. they see a form if they haven't submitted anything, but they see a list of things if they have?**

They will be greeted by a home page or start menu, then move into the game where each player will have a chance to guess their individual score. At the end of each round, the game status screen will be shown and the user will be able to click a button and move to the next round. At the end of the game there will be a final conclusion screen where the user or users are offered the chance to play again.

## Extras

* **Why might your application send email?**
My application might send an email to a player if they currently hold a high score, and it has been broken by another player

* **If you plan to have user accounts, what information will be specific to a user account? What can you only see if you're logged in? What will you see if you're not logged in -- anything?**
The information that will be specific to user accounts will be name, highscore, and email. You will be able to 
play as a guest if you do not wish to put your information into the game,
* **What are your biggest concerns about the process of building this application?**
my biggest concerns lie in the difficulty of creating a complete game like this. Game development can often take a very long time, and I think it will be very complex to build this whole working system out.
