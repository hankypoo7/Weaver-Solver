# Weaver Solver
A solver for any challenge of the weaver game. The game can be played at [wordwormdormdork.com](http://wordwormdormdork.com/) or [weaverwordle.com](http://weaverwordle.com/).
The game is a "word ladder" game.
### Rules
You have to weave your way from the strating word to the ending word. Each word inbetween can only change 1 letter from the word above.

## FAQ
### How does the game work?
Check out the tutorials on [wordwormdormdork.com](http://wordwormdormdork.com/) or [weaverwordle.com](http://weaverwordle.com/), they have a very comprihelsible explanation.

### Why can't I connect 2 words?
Sadly, not all words can be connected. Some words have no connections at all (like `envy`, or `iglu`) and other words are part of only a small group (like `icon, iron, ikon` or `oxid, oxim`). If this happens during a real game though (where a solution must be present), please open an issue. 

### Why does the game say there is a shorter connection?
If this happens, it likely is an issue with the search algorithm. Please open an issue if you find a case, where the calculation is wrong. I will look into it as soon as I find the time.

### What is the longest distance between 2 words?
This is a really interesting problem to solve, because the computation neccessary to connect every word with each other grows large very quickly. The answer is 17 steps! The paths include `unau -> whoa`, `unau -> atom`, `unau -> inch`, and a few more. unau is a type of sloth by the way, and yes it is part of every of these longest paths.

### How does this work?
In the code, there is a list of all possible words. While searching, we do a bidirectional BFS, meaning a breadth-first search from both ends of the weave until we meet in the middle and find a valid path from one to the other. Due to the paths having no weights, and the branching nature of the graph, this is a really fast and efficient approach.

### Why are you ruining the game by giving out the solution?
because I'm better at coding than I am at word games.
