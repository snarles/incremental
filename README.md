# incremental
Python tools for automatically testing and generating javascript games

*Introduction*

The goal of this project is to provide some tools for designing single-player games which can be
automatically tested by artificially intelligent players.

A typical game might be the following: a player explores a world by clicking on various locations in the game;
interacts with other characters via menu-based choices, and completes their goals by means of acquiring various
resources, choosing the right attacks to use in combats, etc.  The game will also including a timing element:
players may automatically accumulate resources over time, and their abilities may produce effects with a timed
duration.

The success of any game depends on many factors: an engaging story, immersive graphics and audio,
or gameplay that creates emotional suspense.  But the main goal of this project is to address
the prescence of strategically interesting choices in the game.  These kinds of choices occur when
the player is aware of more than one way to achieve his immediate goal: now they can try to decide
which choice will provide the most additional benefits to them.  A typical example might be when a player
can choose a strategy for defeating a difficult enemy: 1) she can choose to strengthen his character
by finding a good lcoation in the game for training; 2) she can spend some money to buy a better weapon,
or 3) she can consume one of her items, a "bomb", to defeat the enemy: this way is the fastest,
but then the player will no longer be have the bomb at her disposal in a later battle.

A mere multiplicity of options does not guarantee that the choices will be interesting.
A common problem in big budget and homebrewn games alike is poor "balance" throughtout the game:
although, in principle, there are many routes to the same goal, one route in particular
is obviously much better than all other choices.  But it is extremely difficult for a game designer
to assess balance without personally testing the game, or getting feedback from playtesters.

We propose that tools for computer "simulations" of playthroughs of the game can help designers get a feel
for the dynamics of their game.  The main challenge is modeling a player's behavior via
a computer algorithm.  The main assumption we need is that the player will attempt to play "optimally:"
for instance, attempting to complete the game in the shortest amount of time.

To carry out the simulations, we require the game to be described formally as a system
consisting of 1) player actions, 2) hidden game variables and 3) "visible" game variables,
plus game mechanics which describe how the system evolves through time in response to player actions.
Using our tools, the game designer can then specify an artificially intelligent agent
which attempts to choose its game actions to optimize its goals.  By seeing the
playthroughs of the game made by the AI, the game designer can discover unexpected features or
problems in her game design.

However, this seemingly requires the game designer to spend double the effort in implementing the game:
once for human-playable version, and one for the formal version intended for testing, not to mention
having to synchronize any changes made to either version.  Therefore our second proposal is
to provide tools for automatically generating the human-playable version of the game from
the formal description of the game, combined with designer-specified "templates" for handling the implementation.


