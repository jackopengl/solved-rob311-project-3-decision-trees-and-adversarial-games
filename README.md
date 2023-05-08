Download Link: https://assignmentchef.com/product/solved-rob311-project-3-decision-trees-and-adversarial-games
<br>
<h1>Part 1: Decision Tree Learning</h1>

Decision trees are useful for a wide range of machine learning tasks, and have the advantage of being readily understandable by people. We will be concerned with building trees using training data involving discretevalued attributes only. You will implement functions to determine how to split the data (and build the tree) based on the information gain and gain ratio criteria. Your tasks are to:

<ol>

 <li>Implement five basic support functions for decision tree learning that compute (in order): discrete entropy, conditional entropy, intrinsic information, information gain, and information gain ratio. Use the function templates py in the handout code to get started.</li>

 <li>Implement a Python version of the Decision Tree Learning algorithm given on pg. 702 of the AIMA text, in the file py. Your learning implementation will make use of the functions provided above (and enable splitting using both information gain and gain ratio criteria).</li>

</ol>

Some utility code has been provided for you in the form of a TreeNode class and its methods, and a function to compute the ‘plurality value’ of a set of examples (do not modify these). Please read all comments in the starter code for implementation details. You will submit your implementations of all 6 template functions in decision_tree.py through Autolab.




<h1>Part 2: Adversarial Games</h1>

One of the fist applications of AI was to games, and many well known games have now been solved (e.g., you can read the fascinating story about solving checkers <a href="https://www.theatlantic.com/technology/archive/2017/07/marion-tinsley-checkers/534111/">here</a>). That is, the optimal set of moves given any starting state is known. However, developing game-playing agents can still be challenging! In this open-ended portion of the project, you will write an agent to play a modified version of rock-paper-scissors with a game (payoff) matrix of the form:

<h2>                                                                              <strong>M </strong><em> ,                                                   </em>(1)</h2>

where <em>a</em>, <em>b</em>, and <em>c </em>are all positive (you will not be given their values). Your task is to:

<ol>

 <li>Write a game-playing agent that attempts to win as many games as possible. The class StudentAgent in iterated_single_move_games.py has three methods that you must implement. As usual, you may only use the import statements present in the file.</li>

</ol>

Your agent will be pitted against other agents: for each given opponent, your StudentAgent class will repeat

1000 rounds against that opponent. See the play_game function in iterated_single_move_games.py for details. The other agents you are up against are:

<ul>

 <li>a dumb agent that always chooses the first move (see FirstMovePlayer),</li>

 <li>a copycat agent that always copies its opponent’s last move (see CopycatPlayer),</li>

 <li>an agent that randomly chooses one of the three options with equal probability (see UniformPlayer),</li>

 <li>a ‘goldfish’ agent with very short memory (source code is not available to you),</li>

 <li>an agent that uses a mixed Nash equilibrium strategy (source code is not available to you),</li>

 <li>and an agent that follows a random Markov process that depends on the last round (source code is not available to you).</li>

</ul>

You do not have to beat every agent head-to-head, but you must win the lion’s share of the points (see the Grading section below). The exact strategy that your agent employs is a design decision—however, you must briefly document the technique(s) you used in your code (see the Grading section below). Please read all the comments in the starter code for implementation details. As the final part of the project, we will hold a round-robin tournament for bonus marks (and glory!).