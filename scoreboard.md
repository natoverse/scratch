# scoreboard

This is a set of sprites for building a game scoreboard. You could use it to keep track of how many items you've collected, or how many enemies you have killed.

There are three sprites: one each to track the `ones`, `tens`, and `hundreds` digits of your score.

In order to increase your score using these scoreboard sprites, you need to broadcast the message `score-increment`. Each sprite will receive that message, keep track of the current score, and update itself as needed<sup>1</sup>. As you can probably guess, every score increment will cause the `ones` sprite to increase its number, and every ten increments will cause the `tens` to increase.

You can use as many as you'd like: if you only want your high score to be **9**, use the `ones` sprite. If you'd like to go up to **99**, put a `tens` sprite to the left of your `ones` sprite. And of course, if you'd like your score to go all the way to **999**, put the `hundreds` sprite to the left of that. Want to go even higher? I'll leave it to you to figure out how to create a `thousands` sprite using these as your example.

## Other things to try

* How about using a `score-decrement` message to decrease the score? What logic would you need to put in each sprite for that to work?
* This example uses the letter sprite provided by Scratch—what about creating your own digit sprites so you have a completely custom scoreboard?

___

<sup>1</sup>Note that each sprite really does track the score on it's own—they each have their own private `score` variable to keep track of, so they can be loaded and used individually.
