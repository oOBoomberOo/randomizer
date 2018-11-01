# This datapack is all about generating random number!

# 1) Scoreboard
  [Objective]
    this datapack have only one scoreboard objective called "bb.variable" if you see anything about scoreboard you can always assume we're talking about this objective
  [Selector]
    Selector will always have "#" symbol infront of their name and you can somewhat guess what it does from just reading the name itself. 
    For example "#boomber.randomizer.random_1.input.min" from this name I know that it from me! or "boomber" from a datapack called "randomizer" from method "random 1" and it's an input of minimum range of random number generator.
    Again if you see "#" you can assume that we're talking about scoreboard

# 2) Random number generators
  1. Random 1 \| In-game Pseudo-random number generator
  
    This method use "Linear congruential generator" algorithm to generate random number.
	
    [Pros]:	
     \- no entity required
    [Cons]:
     \- the result is less random than others method

    1. Genereate random number
	  Simply run "/function boomber:randomizer/random" This will generate random number with default setting which is random number between 0 - 10.

      You can also run /function boomber:randomizer/random/[0-99, 0-100, custom] to generate random number with different range, the first two are exactly what the name state generate random number between 0-99 and 0-100 but custom allow you to generate number between any range you want.

      [Input] to tell /function boomber:randomizer/random/custom the range you want your random number to be
       \- #boomber.randomizer.random_1.input.min
          min range of random number
          usage: /scoreboard players set #boomber.randomizer.random_1.input.min bb.variable <n>
       \- #boomber.randomizer.random_1.input.max
          max range of random number
          usage: /scoreboard players set #boomber.randomizer.random_1.input.max bb.variable <n>
        note: max input should always be (max range + 1) because some math stuff.

# 3) Retrieving generated number
  "#boomber.randomizer.result" is where all the generated number will be and then you can just run /scoreboard players get #boomber.randomizer.result bb.variable to get that generated number