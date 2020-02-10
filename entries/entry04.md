# Entry 4
##### 2/9/20

### Update
During the past few weeks me and my partner had been playing around with Halite. Generally what we did was adding algorithms that help dictates the movement of the ships. For example, some ships would often get stuck due to the fact that the base and its surrounding are occupied by a ship making it impossible for the ships to move. The algorithm that helps solve this issue is actually a built-in method where it instructs ships to swap locations. This freed up spaces around the base and prevented clogging. Another function that my partner implemented was the ability to chunk the map. By chunking the map the ships will go to the highest density location and get the most yield. See more in depth explanation through [ZhiYuan’s Blog Entry 4](https://github.com/zhiyuanc1718/apcsa-freedom-project/blob/master/entries/entry04.md). This basically concludes our progress for the past few days. <br><br>

Something that we also did was logging the game to a .txt file hoping that it will come of use when feeding it to the AI.


```Python
        # writing file
        f = open("gameinfo" + str(game.my_id) + ".txt", "w+")

        for areaCode in Halite:
            f.write("Area Code: " + str(areaCode) + ", Halite: " + str(zoneHalite[areaCode]) + "\n")

        f.write("Total Halite in game map = " + str(maxHalite) + "\n")
        highHaliteZone = highestDensityZone()
        f.write("Highest Halite within one Area: " + str(highHaliteZone[0]) + "\n")
        for z in highHaliteZone[1]:
          f.write("Highest Halite Value Area Code: " + str(z) + "\n")

        f.write("My ships will avoid the following coordinates \n")
        for coords in avoidCoords:
          f.write(str(coords) + "\n")

        shipyard = []
        for player in game.players:
          shipyards.append(gam.players[player].shipyard.[position])

        for base in shipyards:
          f.write("shipyard location: (" + str(base.x) + "," + str(base.y) + "\n")
        f.close()

```

### Most Recent Steps
Personally I have started looking into Machine Learning where I found [sentdex’s tutorial](https://pythonprogramming.net/machine-learning-tutorials/) and [Joshua Stoker's documentation](https://stakernotes.com/diamond-ranked-ml-for-halite3/) to be really helpful. sentdex is a content creator on Youtube with many tutorials on python applications such as machine learning. He also has a website that logs his code along with his explanation. Joshua Stoker has a really in depth explanation as to how you can apply machine learning to Halite 3 specify. <br><br>

### Engineering Design Process
As of current we are reaching the end of the **prototype** stage. The purpose of building a bot gets a feel for the mechanics behind Halite and enriches our understanding of Python. Moving on we will be finally going into machine learning to program our bot.<br><br>

### Skills
In terms of skills me and my partner had gained quite a few over these weeks. We were challenged by the actions of the bot having to find **creative** solutions to change whatever is necessary. **Debugging** skills is also involved in making the code work. Often it's the smallest thing like indentation that led to error logs.<br><br>

### Knowledge
Generally saying there is hardly any difference in Python and Java. Something that I find interesting that Java doesn’t have is a range() method. This method is responsible for printing a sequence. This method is often accompanied by for loops which makes it really helpful. Java on the other hand does need this since it is for loop you can set the sequence yourself. <br><br>
```Python
    x = range(3, 20, 2)
    for n in x:
        print(n)
    # Prints 3 to 19 by increment of 2

```

### New Tools!

[TensorFlow](https://www.tensorflow.org/) is a framework for machine learning that simplifies the process in building a Neural Networks. We resorted to using TensorFlow because building a Neural Network requires extensive knowledge on Mathematics. Other frameworks like Pytorch can do the job but lacks the community that we are looking for.<br><br>

[Keras](https://keras.io/) is a Neural Network API that will be running on top of TensorFlow. It has pretrained models that can help shorten the time of training. Inside Keras’s Documentation you can find important details about its build-in method as well as initializing the pre-trained model. The pre-train models can be used in our code to speed up the learning process.<br><br>

[Numpy](http://cs231n.github.io/python-numpy-tutorial/) is a library for Python that gives the user the ability to include multi-dimensional array and matrices(2-d arrays). This Library is generally used in Machine Learning or any other application with high-level of math.<br><br>

[Jupyter NoteBook](https://jupyter.org/documentation) serves as a dynamic way to view your code. It is widely used for the purpose of ML. The selling point is its ability to chunk your code and make visual representation of data with the help of Python libraries.<br><br>

### Upcoming Plan
Moving forward we hope to complete a prototype of the Machine Learning bot by the next blog entry. As usually more information about the new tools can be found through their official website.



[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)