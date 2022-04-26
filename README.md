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
- This Python script is using IMDb movie all time Top 250 movies as rated by regular IMDb voters.
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
then importing IMDb library:
```
pip install cinemagoer
import imdb
ia = imdb.Cinemagoer()

```

- *NOTE:  If a package does not come pre-installed with Anaconda, you'll need to provide instructions for installing that package here.*

We then import data from [insert name of data source].  We print the data to allow us to verify what we've imported:
```
x = [1, 3, 4, 7]
y = [2, 5, 1, 6]

for i in range(0,len(x)):
	print "x[%d] = %f" % (i, x[i])		
```
- *NOTE 1:  This sample code doesn't actually import anything.  You'll need your code to grab live data from an online source.*  
- *NOTE 2:  You will probably also need to clean/filter/re-structure the raw data.  Be sure to include that step.*

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

- *NOTE: You are welcome to provide instructions using Anaconda or IPython.*

---

## Suggestions
*Finally, you should suggest any additional features that would be useful/interesting.  For example, what else could you do with these data?  How might you want to modify the plot to be more descriptive?  What summary statistics might you want to calculate with these data?*
This sorce code and package can be used for creation of new trivia games. You can use other data like year of movie or change the sequence of what is given and what player has to guess in similar way. For example, you can swicth the game about actors - give an actor and provide with 4 movies which he might be playing at. Or a with a bit more of changes you can give year of first on the screen and then let choose the right one.
