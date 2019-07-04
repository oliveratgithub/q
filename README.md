quizbot
=======

Small and simple quizbot for IRC
--------------------------------


Use
===

Hack [config.py](config.py) to your liking (it's pretty self-explanatory).

Write questions  in [questions.py](questions.py), as per the format.
*Note*: you need at least eleven question for quizbot to work properly.

Start the bot with:
`$ ./q`
or
`$ python q`

Start and keep the bot running in a background task:
`$ nohup ./q &`
or
`$ python ./q &`

IRC
----

Join the same channel where quizbot is connected to.

*Note*: channel users with nick names as defined in the config under `masters=[]` can control the bot, e.g. force a reload of the questions.

`!help` : lists available commands

Masters commands:
`!op` : OP a master.
`!deop` : DEOP a master
`!reload` : Reload the question/answer list.

General commands:
`!score` : Print the top five quizzers
`!hiscore` : Print the top five quizzers of all time
`!botsnack` : Feed quizbot to keep it going

Dependencies
============

quizbot is written in Python and runs on the 2.7 interpreter. The dependencies 
below are listed with the oldest versions that are confirmed to work. Older 
versions *might* work. If they do, please report it to <alexander@plaimi.net>, 
so that he can update this file.

- python 2.7.x
- twisted >= 11.0.0
`$ apt-get install python-twisted`
- twisted-words >= 11.0.0
`$ apt-get install python-twisted-words`

A Note on Python 3
------------------

The 3.x interpreter will try to run this and fail. You *need* to use a 2.x 
interpreter (2.7.x is the only one with which quizbot is formally tested). 
This may be accomplished by specifically invoking a 2.x interpreter on some 
systems.
`$ python2 q`


quizbot in #quiznode on Freenode
================================

My quizbot instance runs in the #quiznode channel on irc.freenode.net:6667.  
Feel free to check it out and come play. :-)

Send questions and answers to me via email (see Author), so that quizbot has 
more to choose from. I think it's more fun to let you guys decide what you are 
interested in quizzing about, rather than parsing someone else's trivia 
questions. Us the format of questions.py, or send me a diff. At the very 
least, make sure you have "category - question - answer" or something like 
that.

Happy quizzing!


Contributing To the Project
===========================
Yes, please. Follow PEP-8: <http://www.python.org/dev/peps/pep-0008/>.

- Improve the way question-answer pairs are stored. (Please provide code to
  convert the current structure for me to test it.)
- Write better algorithms for detecting answers.
- Make quizbot reconnect correctly when it loses its IRC connection.
- Improve ugly parts of the code (there's plenty to choose from).
- Improve commenting by to be more clear and/or informative.

Try to keep the source very short. Please take some time to come up with the
shortest readable and logical solution to what you are trying to do. When you
are finished, send me a pull-request using Github or an email (see Author).

Please write sane commit messages. An introduction to git commit messages: 
<http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html>. Do 
small commits, and only working commits. No WIP-code. NOT IN MY BACK... 
repository...

If you want to report a bug, use <https://secure.plaimi.net/bugs>.  If you 
want to discuss some the game, give us suggestions etc. -- use 
<https://secure.plaimi.net/mailing.php>.

Happy hacking!


Licensing and Legalese
======================

quizbot is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

quizbot is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with quizbot.  If not, see <http://www.gnu.org/licenses/>.


Author
=======

Alexander Berntsen <alexander@plaimi.net>

/* vim: set textwidth=78 formatoptions=actw2 autoindent: */
