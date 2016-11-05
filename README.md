
# TOURNAMENT

Fouth Project of Full Stack Web Developer NanoDegree

## TOURNAMENT PROJECT SPECIFICATION

Develop a database schema to store details of a games matches between players.   
Then write a Python module to rank the players and pair them up in matches in a tournament.

## SWISS-SYSTEM TOURNAMENT

A non-eliminating tournament format which features a predetermined number of rounds of competition, but considerably fewer than in a round-robin tournament. In a Swiss tournament, each competitor (team or individual) does not play every other. Competitors meet one-to-one in each round and are paired using a predetermined set of rules designed to ensure that each competitor plays opponents with a similar running score, but not the same opponent more than once. The winner is the competitor with the highest aggregate points earned in all rounds. All competitors play in each round unless there is an odd number of them.

## FILES

**tournament.py**  

Contains the implementation for the Swiss tournament  

**tournament.sql**  

Contains the SQL queries to create the database, tables and views   

**tournament_test.py**  

Contains the test cases for tournament.py  

##Functions in tournament.py

**registerPlayer(name)**

Adds a player to the tournament by putting an entry in the database. The database should assign an ID number to the player. Different players may have the same names but will receive different ID numbers.

**countPlayers()**

Returns the number of currently registered players. This function should not use the Python len() function; it should have the database count the players.

**deletePlayers()**

Clear out all the player records from the database.

**reportMatch(winner, loser)**

Stores the outcome of a single match between two players in the database.

**deleteMatches()**

Clear out all the match records from the database.

**playerStandings()**

Returns a list of (id, name, wins, matches) for each player, sorted by the number of wins each player has.

**swissPairings()**

Given the existing set of registered players and the matches they have played, generates and returns a list of pairings according to the Swiss system. Each pairing is a tuple (id1, name1, id2, name2), giving the ID and name of the paired players. For instance, if there are eight registered players, this function should return four pairings. This function should use playerStandings to find the ranking of players.

## INSTRUCTIONS

1. Start Vagrant
  1. Open Terminal or cmd and browse to the vagrant folder
  2. Type `vagrant up`
2. SSH in to the vagrant VM
  1. In the same terminal type `vagrant ssh`
3. Change to the correct folder
  1. Type `cd /vagrant/tournament`
4. Open PSQL and run the tournament.sql 
  1. type `psql`
  2. copy the contents of tournament.sql and paste in to the terminal window
  3. type `\q` to quit out of PSQL 
5. Run the tests
  1. In the terminal type `python tournament_test.py`


