# BSnake2018
If you aren't in my team, please don't look at / copy / learn from / learn to counter this snake. thanks!

Instructions on how to start development:

Install Git, and clone the repository.
Install Go. I started going through the instructions, but in the end that didn't work but apt install golang-go did so that's cool.

To Develop: Make a branch corresponding to a needed task. Don't overlap a task someone else is already doing!
git checkout -b "branchname"
then add your changes and commit it to this repo on github.
Then create it as a pull request for everyone to debate over.
Then once it's been accepted, merge it in!


Big Roadblocks
 - AWS - how do we deploy to it, how do we get AWS to talk to the arena, how many threads can we use, how much will a really powerful instance cost, what's the time delay between AWS and the arena?
 
 Things to do
 
  - Build An Adversarial Search Algorithms
      - build the tree that predicts the moves
           - Build in rules to limit number of snakes, and stop illegal moves. Calculate branching factor.
        
      - build the heuristic that measures the score of each board.
           - build a flood-fill search to check open areas
           
       - build timing functions so we can keep track of how much each step takes.
Go Snake
