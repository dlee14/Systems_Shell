# Systems_Shell
Kevin Li and Peter Lee
<br>
Period 10

<h2> Features </h2>
<ul>
<li> Forks and executes commands </li>
<li> Has a nice greeting when you open the shell! </li>
<li> Handles cd and exit </li>
<li> Displays working directory, like bash </li>
<li> San execute multiple commands on one line separated with semicolon (";") </li>
<li> Says something nice when you quit shell! </li>
<li> When you do something bad in the shell, it will print out bash-like errors using errno </li>
<li> magic can hide or show your working directory </li>
</ul>

<h2> Attempted </h2>
<ul>
<li> Handle multiple commands on one line when semicolons are surrounded with spaces, like " ; " instead of just ";" </li>
<li> Redirection and pipes </li>
</ul>

<h2> Bugs </h2>
<ul>
<li> Very occasionally the parser fails and cannot read the commands correctly. We tested it, and every time it happens, it can't read a certain character and reads it as a space. </li>
<li> Cannot handle multiple commands on one line when semicolon is surrounded by spaces. </li>
</ul>

<h2> Files and Function Headers </h2>
<h3> main.c </h3>

<h3> shell.c </h3>

<h4>char ** parse_args(char * line, char delimiter)</h4>
  <ul>
  <li>Description:</li>
    <ul>
      <li>Parses the given string using the given delimiter</li>
    </ul>
  <li>Arguments:</li>
    <ul>
      <li>char * line -> A pointer to the original string</li>
      <li>char delimiter -> The character that is going to be used to parse the string</li>
    </ul>
  <li>Return Value:</li>
    <ul>
      <li>A char ** which consists of the parsed strings</li>
    </ul>
  </ul>
  
<h4>void exec_one(char ** args)</h4>
  <ul>
  <li>Description:</li>
    <ul>
      <li>Forks off a child process and the child process calls execvp to execute the given command</li>
    </ul>
  <li>Arguments:</li>
    <ul>
      <li>char ** args -> Command line arguments that should be executed</li>
    </ul>
  <li>Return Value:</li>
    <ul>
      <li>N/A</li>
    </ul>
  </ul>
