# BSnake2018
If you aren't in my team, please don't look at / copy / learn from / learn to counter this snake. thanks!

Instructions on how to start development:

Install Git, and clone the repository.
Install Go. I started going through the instructions, but in the end that didn't work but apt install golang-go did so that's cool.

https://github.com/sendwithus/battlesnake-go


Compile the battlesnake-go server.

    go build

This will create a battlesnake-go executable.

Set your snake ID as an environment variable.

    export SNAKE_ID=ABCDEF1234

This will allow your snake to locate itself during the game.

Run the server.

    ./battlesnake-go

Test the client in your browser: http://127.0.0.1:9000


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
           - This should also keep track of "narrowness", e.g. if the snake has to move through a lot of narrow spaces to get here.
        
      - build the heuristic that measures the score of each board.
           - build a flood-fill search to check open areas. space for us is good, space for competitors is bad.
           - Take into account health of all snakes.
           - Could take into account new rules such as coins.
           - Take into account the amount of narrowness that the snake had to go through to get there.
           
       - build timing functions so we can keep track of how much each step takes.
Go Snake
