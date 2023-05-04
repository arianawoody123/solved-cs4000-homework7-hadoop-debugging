Download Link: https://assignmentchef.com/product/solved-cs4000-homework7-hadoop-debugging
<br>
Email and other electronic media are often filtered for offensive language using fast, but relatively simple means (think finite automata). However, these simple filters are easily tricked. For example, if your filter was looking for the phrase “bad language,” you could trick it by inserting characters between the letters, e.g., by writing “..b..a..d…l..a..n..g..u..a..g..e…”. In this case, this text is easily recognizable by a human as the words “bad language”, but harder (but not impossible) to recognize by a simple filter.

For this assignment, you are looking for potential “secret messages” embedded into tweets (both real and simulated). In particular, you are trying to find which Twitter users are posting “secret messages” to their followers. You discovered that, given a string, such as “secretMESSAGE”, you can see whether those letters are embedded (in that order) in a tweet in <em>O</em>(<em>n</em>) steps, where <em>n </em>is the number of characters in the tweet. You wrote a couple (2) of Hadoop programs to output the number of times each Twitter user tweeted a message that had the string “secretMESSAGE” embedded somewhere in the message. Unfortunately, your little brother Ike got into your account and messed up the program. The first program won’t compile. The second program runs, but it doesn’t get the right answer. You’ll have to fix them.

<h1>The Data Format</h1>

For this assignment, the Twitter data that you will be using has been pre-filtered to remove information about the Twitter user (screen_name) and the text of the tweet. Furthermore, tabs and newlines within the tweet have been converted to spaces. So, the data files for this assignment are provided in a line oriented format, where each line contains the screen name of a Twitter user and the text of tweet, where the screen name and the tweet are separated by a tab character t.

<h1>Part I: Compiling Java Hadoop Programs</h1>

Your first program SecretMessage.java looks for the fixed string “secretMESSAGE” in tweets. The provided program does not compile. It also has some warnings.

<ol>

 <li>(3 pts.) Fix the compilation errors in the file java. What lines did they occur on?</li>

 <li>(3 pts.) Remove the compilation warnings in the file java. What fixes did you make? Explain.</li>

 <li>(3 pts.) Run the Hadoop program on the files txt and random_data.txt. What is the output?</li>

 <li>(1 pt.) How many blocks are used to store txt on the Hadoop Distributed File System?</li>

</ol>

<h1>Part II: Fixing a Broken Hadoop Program</h1>

The second program GeneralMessage.java is intended to be a general version of the first program. As the first commandline parameter, the user passes in a string that replaces the hard-coded “secretMESSAGE” in the first program. To run this second program, issue the command yarn jar program.jar GeneralMessage secretMESSAGE Input Output

Here, “secretMESSAGE” could be anything.

The current program does not run correctly. Fix this program in such a way that it performs just like the original program when using the string “secretMESSAGE” as a commandline parameter, and so that it works on other strings as well.

<ol>

 <li> Fix the program java so that it compiles and runs correctly. What lines in the program did you fix? Be specific.</li>

 <li> Run the corrected program on the files txt and random_data.txt and the string “ScaryMess”. How many users have tweets that match that string? Give one of them.</li>

 <li>Run the corrected program on the files txt and random_data.txt and the string “SecretMessage”. How many users have tweets that match that string?</li>

</ol>

Give one of them.