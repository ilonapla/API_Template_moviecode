# Trivia Game based on IMDb Movies

Authors:  **Ian Unson** and **Ilona Platonova**

---

**NOTE**:  The *italicized* content below is for your reference only.  Please remove these comments before submitting.

---

## Introduction
*The purpose of this section is to provide some information about the data you're exploring.  For example, you should*
- *Describe the type of data that you're importing.* 
- *Describe the source of the data.  Include URLs.*  
- *Explain how recent is this data?  How often is it updated?*
- This Python script is using [IMDb movie](https://www.imdb.com/) all time Top 250 movies as rated by regular IMDb voters.
- It creates a trivia game where a single Player is provided with a name of the movie and four alternative actors, one of whom is playing a role in the movie. Player has to choose one of for letters (A, B, C, D) to choose the answer. If it is correct, game is over. If he gets it wrong, he can try again to guess who is the right actor.
- Information used for the trivia: movie names, lead actor IDs and names are retrieved from the IMDb server during the game, so internet connection has to be available.
- Source of the data is updated daily, however the ratings of top 250 do not change significantly from day to day 

---

## Sources
*In this section, provide links to your references.  For example:*
- The code retrieves data from [IMDb website](https://developer.imdb.com/) via [IMDb API](https://imdb-api.com/)
- The code is based on a Python package [Cinemagoer](https://cinemagoer.github.io/)

---

## Explanation of the Code
*In this section you should provide a more detailed explanation of what, exactly, the above code actually does.  Your classmates should be able to read your explanation and understand what is happening in the code.*

The code, `trivia_game_imbd.py`, begins by downloading [here](https://cinemagoer.github.io/) and  installing Cinemagoer package, 
then importing IMDb library FIXME - missing more libraries - random? etc.:
```
pip install cinemagoer
import imdb
ia = imdb.Cinemagoer()

```

- *NOTE:  If a package does not come pre-installed with Anaconda, you'll need to provide instructions for installing that package here. FIXME - do we explain explicitely as I did or should we have more details?*

We then import data from [IMDb api](https://imdb-api.com/).  
```
top_m = ia.get_top250_movies()
```
We select one of the movies ID as the one to play and request from database the title of the movie and main character's name:
```
•FIXME• top_m = ia.get_top250_movies()
```
Then we generate random numbers and select other movies from the list that we take the characters' names from.
Those movies and their cast are sources of our "wrong answers". 
```
•FIXME• top_m = ia.get_top250_movies()
```
Choices are being randomly assigned to variables.
Output on the screen shows the Player four alternatives. He has to input one letter as his choice.
Received keyboard action is compared with variables and check if the correct letter is provided.
If answer is correct player gets response
```
•FIXME• top_m = ia.get_top250_movies()
```
If he is wrong, another trial is possible.


*FIXME - this is professors code - left for example - should be removed until section "how to run code"*

We print the data to allow us to verify what we've imported:
```
x = [1, 3, 4, 7]
y = [2, 5, 1, 6]

for i in range(0,len(x)):
	print "x[%d] = %f" % (i, x[i])		
```
- *NOTE 1:  This sample code doesn't actually import anything.  You'll need your code to grab live data from an online source.*  


Finally, we visualize the data.  We save our plot as a `.png` image:
```
plt.plot(x, y)
plt.savefig('samplefigure.png')	
plt.show()
```

The output from this code is shown below:

![Image of Plot](images/samplefigure.png)

---

## How to Run the Code
*Provide step-by-step instructions for running the code.  For example, I like to run code from the terminal:*
1. Open a terminal window.

2. Change directories to where `trivia_game_imbd.py` is saved.

3. Type the following command:
	```
	python trivia_game_imbd.py.py
	```
4. Game is started with generated information about the movie and the alternative actors which to guess.
5. Player can enter information and when the answer is correct, the code stops.

- *NOTE: Please note that all the content of the data is owned by IMBd and API free access allows to run up to 100 requests per day. More requests per day are available for a subscription fee.*

---

## Suggestions
*Finally, you should suggest any additional features that would be useful/interesting.  For example, what else could you do with these data?  How might you want to modify the plot to be more descriptive?  What summary statistics might you want to calculate with these data?*
•This sorce code and package can be used for creation of new trivia games. 
•You can use other data like year of movie or change the sequence of what is given and what player has to guess in similar way. For example, you can swicth the game about actors - give an actor and provide with 4 movies which he might be playing at. 
•With more coding you can use year of first on the screen and then let choose the right one.
