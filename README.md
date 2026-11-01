<!DOCTYPE html>
<html lang="en"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Fundamentals of Programming I – Chapter 1</title>
<style>
:root{--bg:#fafaf7;--fg:#1d2433;--mu:#5b6475;--ac:#1f5f8b;--card:#fff;--bd:#dfe3ea;--code:#eef2f7;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);color-scheme:light}
@media(prefers-color-scheme:dark){:root:not([data-theme=light]){--bg:#13171f;--fg:#e8ebf1;--mu:#98a2b3;--ac:#6cb4e4;--card:#1b212c;--bd:#2c3442;--code:#232b38;color-scheme:dark}}
:root[data-theme=dark]{--bg:#13171f;--fg:#e8ebf1;--mu:#98a2b3;--ac:#6cb4e4;--card:#1b212c;--bd:#2c3442;--code:#232b38;color-scheme:dark}
html{scroll-padding-top:70px;scroll-behavior:smooth}
body{margin:0;background:var(--bg);color:var(--fg);font:17px/1.65 Georgia,'Times New Roman',serif}
nav{position:sticky;top:env(safe-area-inset-top,0px);background:var(--bg);border-bottom:1px solid var(--bd);padding:10px 16px;display:flex;gap:6px;overflow-x:auto;white-space:nowrap;z-index:5;font:14px system-ui,sans-serif}
nav a{color:var(--mu);text-decoration:none;padding:4px 10px;border-radius:14px}nav a:hover{background:var(--code);color:var(--ac)}
nav b{display:none}
@media(min-width:900px){
html{scroll-padding-top:20px}
body{padding-left:250px}
nav{position:fixed;top:0;left:0;bottom:0;width:250px;box-sizing:border-box;flex-direction:column;gap:2px;padding:calc(24px + env(safe-area-inset-top,0px)) 14px 24px;border-bottom:0;border-right:1px solid var(--bd);overflow-y:auto;white-space:normal;font-size:15px}
nav b{display:block;font:700 12px system-ui;letter-spacing:.08em;text-transform:uppercase;color:var(--ac);padding:0 10px 10px}
nav a{border-radius:8px;padding:8px 10px}
}
header{max-width:820px;margin:0 auto;padding:48px 20px 8px}
header small{font:600 13px system-ui;letter-spacing:.08em;text-transform:uppercase;color:var(--ac)}
h1{font-size:clamp(28px,5vw,42px);line-height:1.15;margin:.3em 0;text-align:center}
main{max-width:820px;margin:0 auto;padding:0 20px 60px}
h2{margin-top:2.4em;padding-top:.4em;border-top:2px solid var(--ac);font-size:26px}
h3{margin-bottom:.2em;font-size:19px}
.card{background:var(--card);border:1px solid var(--bd);border-radius:10px;padding:14px 18px;margin:12px 0}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px}
.grid .card{margin:0}.card h3{margin-top:0;color:var(--ac)}
ol.steps{counter-reset:s;list-style:none;padding:0}
ol.steps li{counter-increment:s;margin:8px 0;padding-left:44px;position:relative}
ol.steps li:before{content:counter(s);position:absolute;left:0;top:0;width:30px;height:30px;border-radius:50%;background:var(--ac);color:var(--bg);font:700 15px/30px system-ui;text-align:center}
.tw{overflow-x:auto}table{border-collapse:collapse;width:100%;font-size:15px}
th,td{border:1px solid var(--bd);padding:8px 10px;text-align:left;vertical-align:top}th{background:var(--code);font-family:system-ui}
pre{background:var(--code);padding:12px 16px;border-radius:8px;overflow-x:auto;font:14px/1.5 ui-monospace,Menlo,monospace}
details{background:var(--card);border:1px solid var(--bd);border-radius:10px;padding:10px 16px;margin:10px 0}
summary{cursor:pointer;font-weight:700;color:var(--ac);font-family:system-ui}
.fc{display:flex;flex-direction:column;align-items:center;font:14px system-ui;gap:0}
.fc div{padding:6px 16px;border:2px solid var(--ac);background:var(--card);text-align:center}
.fc .t{border-radius:20px}.fc .io{transform:skewX(-12deg)}.fc .io span{display:inline-block;transform:skewX(12deg)}
.fc i{width:2px;height:16px;background:var(--ac)}
.tip{background:var(--code);border-left:4px solid var(--ac);border-radius:6px;padding:10px 16px;margin:14px 0;font-size:16px}.tip b:first-child{display:block;font:700 12px system-ui;letter-spacing:.08em;text-transform:uppercase;color:var(--ac);margin-bottom:2px}dt{font-weight:700;margin-top:10px}dd{margin:0 0 0 18px;color:var(--mu)}
footer{text-align:center;color:var(--mu);font:14px system-ui;padding:30px 20px}
button{font:14px system-ui;background:var(--code);color:var(--fg);border:1px solid var(--bd);border-radius:14px;padding:4px 12px;cursor:pointer;float:right}
</style></head><body>
<nav><b>Chapter 1 contents</b><a href="#sdlc">Program development</a><a href="#analysis">Problem analysis</a><a href="#algo">Algorithms</a><a href="#flow">Flowcharts</a><a href="#practice">Exercises</a><a href="#langs">Languages</a><a href="#paradigms">Paradigms</a><a href="#refs">Resources</a><a href="#gloss">Glossary</a></nav>
<header>
<h1>Chapter One<br>Basic Concepts of Programming</h1>
<p style="color:var(--mu);text-align:center">Problem analysis, algorithm design, pseudocode, flowcharts, and an overview of languages and paradigms.</p><div class="tip" style="margin-top:24px"><b>New to programming? Start here</b>You need no prior knowledge. Read each section in order, and look for the shaded boxes like this one: they explain the ideas in plain words with everyday examples. Do the exercises with pen and paper before opening the answers. This chapter has no real code yet. It teaches you to plan a solution, which is the most important programming skill. A short glossary and self-check questions are at the end.</div></header>
<main>
<h2 id="sdlc">1. Basics of program development</h2>
<div class="grid">
<div class="card"><h3>Computer program</h3>A self-contained set of explicit, unambiguous instructions telling the computer what to do and how.</div>
<div class="card"><h3>Computer programming</h3>Also called coding: writing, testing, debugging, troubleshooting and maintaining source code.</div>
<div class="card"><h3>Software development life cycle</h3>The overall process of developing software, from planning to maintenance.</div></div>
<div class="tip"><b>In plain words</b>A program is like a recipe. A recipe lists ingredients and exact steps, and a cook follows them without guessing. A computer is a very fast cook that does exactly what the steps say, nothing more. If a step is unclear or missing, it will not guess what you meant. That is why the instructions must be explicit and unambiguous.</div>
<h3>Why study programming?</h3>
<ul><li><b>Great job prospects:</b> computers are nearly everywhere.</li><li><b>It makes things easier:</b> chatting, appliances and car locks all run programs.</li><li><b>It develops thinking:</b> structured, logical, creative, and persistent.</li><li><b>You learn how to learn</b> and become more detail-oriented.</li></ul>
<h3>Program development life cycle</h3>
<ol class="steps"><li><b>Planning:</b> gather information from stakeholders; decide what is feasible.</li><li><b>Requirements analysis:</b> collect and document requirements.</li><li><b>Design:</b> create the architecture of the system and its elements.</li><li><b>Implementation:</b> build the software in a programming language.</li><li><b>Testing and integration:</b> evaluate quality; find and fix defects.</li><li><b>Maintenance:</b> update and support the software after release.</li></ol>

<div class="tip"><b>In plain words</b>The life cycle is how a team builds software without chaos, much like building a house: decide what you can afford (planning), ask the owner what they need (requirements), draw the plans (design), build (implementation), inspect (testing), and repair and improve over the years (maintenance). Real projects often loop back to earlier steps when something changes. As a beginner, you will mostly practice the middle steps on small programs.</div>
<h3>A deeper look at the life cycle</h3>
<p>Professional developers group the work into three overlapping phases: <b>development and design</b> (analysis, design, coding, testing), <b>documentation</b>, and <b>maintenance</b>. They overlap in time. Documentation starts during design and continues until the program is retired.</p>
<details><summary>Feasibility study: is the project worth doing?</summary>Before building a large system, the team checks four things. <b>Organizational:</b> does it support the organization's goals? <b>Economic:</b> will it save money or raise profit? <b>Technical:</b> do we have the hardware, software and network to run it? <b>Operational:</b> will users and management accept it, and does it meet customer and government requirements?</details>
<details><summary>Testing and debugging</summary><b>Testing</b> checks whether the program is correct. <b>Debugging</b> means locating, correcting and re-checking an error (a bug). Testing every possible case is impossible for most programs, so we choose test data carefully, and good teams plan their test data before writing the code. Testing happens in levels: <b>unit testing</b> (each small part alone), <b>integration testing</b> (parts combined, to check they work together), <b>system testing</b> (the whole system on its real platform) and <b>acceptance testing</b> (does it do what the user needs?).</details>
<details><summary>Documentation: five key documents</summary>1. The algorithm and its changes. 2. A program description. 3. A well-commented program listing. 4. Sample test runs. 5. A users' manual. Without documentation, work gets lost and tasks must be repeated.</details>
<details><summary>Maintenance: usually the longest phase</summary>Development may take days or months, but maintenance can last years or decades. Programs are changed because of bugs found later, new user needs, organizational change, or new technology. Good documentation makes maintenance faster and cheaper.</details>
<h2 id="analysis">2. Problem analysis</h2>
<p>A problem is the gap between the existing and the desired situation. <b>Problem solving</b> transforms a problem description into a solution, and programming is a form of problem solving:</p>
<ol class="steps"><li><b>Problem analysis:</b> understand the problem; identify input and output.</li><li><b>Algorithm design:</b> design the solution.</li><li><b>Coding:</b> write a program matching the algorithm's steps.</li></ol>
<div class="grid"><div class="card"><h3>Input</h3>What data are available?</div><div class="card"><h3>Process</h3>What method leads from the data to the results?</div><div class="card"><h3>Output</h3>What results must the program produce?</div></div>
<p><b>Why analyze?</b> To understand the real-world problem and user needs, and to validate abstract solutions before development.</p>

<div class="tip"><b>Example: average of two numbers</b><b>Input:</b> two numbers, say 6 and 10. <b>Process:</b> add them, then divide by 2. <b>Output:</b> 8. Whenever you meet a new problem, write down these three things before anything else. Many beginners skip this and start coding too early, and then get stuck because they are not sure what the program should produce.</div>
<h3>More on analysis</h3>
<p>Analysis has two parts. <b>Basic analysis</b> (always needed) extracts the input, the processing and the output. If that is not enough, do an <b>extended analysis</b>: gather more information until you fully understand what is asked. At this stage, focus on <b>what</b> must be done, not <b>how</b>. Record the requirements in a document, and get the users involved.</p>
<h3>Two ways to attack a big problem</h3>
<div class="grid"><div class="card"><h3>Top-down</h3>Start with the whole problem and split it into parts. If a part is still too big, split it again. Solve the small parts, then merge the solutions. Example: <i>class average</i> splits into read the marks, add them, divide by the count, print.</div><div class="card"><h3>Bottom-up</h3>Start by solving the smallest practical parts, then merge them step by step into the final solution. Example: to compute M = &radic;4 + &#8731;4 + &#8308;&radic;4, first find each root, then add the three results.</div></div>
<p style="color:var(--mu)">The main difference is splitting versus merging.</p>
<h2 id="algo">3. Algorithm design</h2>
<p>An <b>algorithm</b> is a well-defined, finite, step-by-step set of instructions that solves a problem or class of problems. It is independent of any programming language. A computer is an "algorithm-responding" machine: it needs detailed step-by-step instructions.</p>
<div class="tw"><table><tr><th>Characteristic</th><th>Meaning</th></tr>
<tr><td>Definiteness</td><td>Each instruction is clear and unambiguous.</td></tr>
<tr><td>Finiteness</td><td>It terminates after a finite number of steps.</td></tr>
<tr><td>Input</td><td>Zero or more inputs.</td></tr>
<tr><td>Output</td><td>At least one well-defined output.</td></tr>
<tr><td>Effectiveness</td><td>Each instruction is basic enough to be carried out.</td></tr></table></div>
<div class="grid" style="margin-top:12px"><div class="card"><h3>Pseudocode</h3>Description of what a program must do in natural language and math symbols; a semi-programming language.</div><div class="card"><h3>Flowchart</h3>Graphical representation: boxes of various kinds, ordered by connecting arrows.</div></div>

<div class="tip"><b>Example: an algorithm for making tea</b>1. Boil water. 2. Put a tea bag in a cup. 3. Pour the water into the cup. 4. Wait 3 minutes. 5. Remove the tea bag. 6. Stop.<br>Check it against the characteristics: every step is clear (definiteness), it ends (finiteness), its inputs are water and a tea bag, its output is a cup of tea, and each step is something you can actually do (effectiveness). An instruction like "make it taste nice" would fail, because it is not definite. A step like "keep stirring forever" would fail, because it never ends.<br><br><b>Pseudocode or flowchart?</b>They describe the same algorithm. Pseudocode is written text and is quick to write. A flowchart is a picture and is easier to follow at a glance. There is no single correct format, so aim for clear, simple steps.</div>
<h3>What makes a good algorithm?</h3>
<p>Besides the five characteristics above, a good algorithm is <b>precise, simple, correct and efficient</b> (it does not waste time or memory). One problem can have many algorithms, so choose one that is easy to maintain and efficient.</p>
<h3>Pseudocode: less formal and more formal</h3>
<p>Pseudocode has no fixed standard. It is not executable, and you may write it informally or formally. Here is the same task, <i>read two integers and print their sum</i>, written both ways. The arrow ← means assign.</p>
<div class="grid"><pre>Less formal
1 Start
2 Ask the user for the first integer
3 Ask for the second integer
4 Work out the sum
5 Display the sum with a message
6 Stop</pre><pre>More formal
1 Start
2 Read n1
3 Read n2
4 sum ← n1 + n2
5 Print sum
6 Stop</pre></div>
<h3>Choosing: largest of two or three numbers</h3>
<div class="grid"><pre>Largest of two
Read n1, n2
if n1 &gt; n2 then
    Big ← n1
else
    Big ← n2
Print Big</pre><pre>Largest of three
Read n1, n2, n3
if n1 &gt;= n2 and n1 &gt;= n3 then
    Big ← n1
else if n2 &gt;= n3 then
    Big ← n2
else
    Big ← n3
Print Big</pre></div>
<p style="color:var(--mu)">Using &gt;= means ties (for example 5, 5, 3) still give the right answer.</p>
<h2 id="flow">4. Flowchart symbols</h2>
<div class="tw"><table><tr><th>Symbol</th><th>Usage</th></tr>
<tr><td>Start / Stop (terminal)</td><td>Beginning and end points.</td></tr>
<tr><td>Process</td><td>An instruction or operation to carry out.</td></tr>
<tr><td>Decision</td><td>A yes/no question with two or more alternatives.</td></tr>
<tr><td>Input / Output</td><td>Read data or print a result.</td></tr>
<tr><td>Connector</td><td>Jump between points, avoiding crossing lines.</td></tr>
<tr><td>Flow arrow</td><td>Shows the direction of instructions.</td></tr></table></div>

<div class="tip"><b>How to read a flowchart</b>Start at the oval marked Start and follow the arrows. Rectangles are actions, slanted boxes are reading or printing, and a diamond is a question with two exits (Yes and No). If an arrow leads back to an earlier box, you have a loop: those steps repeat. Practice by tracing a flowchart with your finger and a sample input.</div>
<h3>More about flowcharts</h3>
<p>There are two kinds. A <b>system flowchart</b> shows the overall logic of a data-processing system. A <b>program flowchart</b> shows the operations and decisions inside one program, and that is the kind used in this chapter. Like pseudocode, a flowchart does not depend on any language, so one flowchart can be translated into several.</p>
<ul><li><b>Decision:</b> a diamond holding a question. It has two exits (True and False), and only one is followed each time.</li><li><b>Connectors:</b> a small circle with a letter links two points on the same page. A pentagon-like shape shows that the chart continues on another page.</li></ul>
<h3>Conventions to follow</h3>
<ul><li>Initialize sums and counters to zero.</li><li>Show assignment with a left arrow (sum ← sum + x).</li><li>Mark the beginning and end of every decision and every repetition, and state its condition.</li><li>Clearly indicate where the algorithm ends.</li></ul>
<h2 id="practice">5. Worked problems and exercises</h2>
<h3>Problem 1: area and perimeter of a rectangle</h3>
<div class="card"><b>Input:</b> Length, Width · <b>Process:</b> Area = L × W; Perimeter = 2 × (L + W) · <b>Output:</b> Area, Perimeter
<div class="fc" style="margin-top:12px"><div class="t">Start</div><i></i><div class="io"><span>Read L, W</span></div><i></i><div>area = L * W</div><i></i><div>perimeter = 2 * (L + W)</div><i></i><div class="io"><span>Print area, perimeter</span></div><i></i><div class="t">End</div></div></div>
<h3>Problem 2: total salary</h3>
<pre>Input: Salary, Overtime
Total_Sal = Salary + Overtime
Output: Total_Sal</pre>
<h3>Problem 3: sum of even numbers from 2 to 30</h3>
<pre>Start
counter = 2, sum = 0
while counter &lt;= 30
    sum = sum + counter
    counter = counter + 2
print sum
End</pre>
<h3>Loops: the four parts</h3>
<p>A loop repeats steps until a condition says stop. A well-formed loop has four parts: <b>initialization</b> (set starting values), <b>computation</b> (the work done each time), a <b>test</b> (every loop must have a way out, or it runs forever) and an <b>update</b> (change the counter so the test can eventually fail). In Problem 3, counter = 2 is the initialization, sum = sum + counter is the computation, counter &lt;= 30 is the test, and counter = counter + 2 is the update.</p>
<h3>Worked example: average of a set of values</h3>
<pre>total ← 0
tally ← 0
for each sample
    total ← total + sample
    tally ← tally + 1
average ← total / tally
print average</pre>
<h3>Worked example: largest and smallest of 50 values</h3>
<pre>Read first number N
MAX ← N, MIN ← N, count ← 1
while count &lt; 50
    Read next number N
    if N &gt; MAX then MAX ← N
    if N &lt; MIN then MIN ← N
    count ← count + 1
Print MAX, MIN</pre>
<p style="color:var(--mu)">Idea: assume the first number is both the largest and smallest, then compare each new number with the best so far.</p>
<div class="tip"><b>Trace Problem 3 by hand</b>To check an algorithm, act as the computer and track each variable on paper. This is called a trace table. The loop begins with counter = 2 and sum = 0. Each pass adds the counter to the sum, then adds 2 to the counter. Before every pass, the computer asks: is the counter still 30 or less?<div class="tw"><table><tr><th>Pass</th><th>counter (before)</th><th>sum (after)</th></tr><tr><td>1</td><td>2</td><td>2</td></tr><tr><td>2</td><td>4</td><td>6</td></tr><tr><td>3</td><td>6</td><td>12</td></tr><tr><td>4</td><td>8</td><td>20</td></tr><tr><td>...</td><td>...</td><td>...</td></tr><tr><td>15</td><td>30</td><td>240</td></tr></table></div>After pass 15 the counter becomes 32, the question "is counter &lt;= 30?" is answered No, and the loop stops. The program prints 240. Always set your starting values (initialize) before the loop, or the result will be wrong.<br><br><b>A method for any exercise:</b>1. Write input, process and output. 2. Write the steps in pseudocode. 3. Test with a small example by hand. 4. Only then draw the flowchart.</div>
<h3>Try it yourself</h3>
<p>Write pseudocode and draw a flowchart for each, then check yourself.</p>
<details><summary>1. Is a number positive or negative?</summary><pre>Start
Read n
if n &gt;= 0 then print "positive"
else print "negative"
End</pre></details>
<details><summary>2. Sum of 1 to n (n = 5 gives 15)</summary><pre>Start
Read n
sum = 0, i = 1
while i &lt;= n
    sum = sum + i
    i = i + 1
print sum
End</pre></details>
<details><summary>3. Bank balance with transactions (ends at 0)</summary>Read the initial balance. Then loop: read a transaction t; if t = 0, stop; otherwise add t to the balance (positive = credit, negative = debit). Finally print the balance. See the slide handout for the full problem statement.</details>
<details><summary>4. Even or odd? (worked)</summary><pre>Start
Read Num
if Num % 2 == 0 then
    print "even"
else
    print "odd"
Stop</pre>% gives the remainder after division. A remainder of 0 means the number divides evenly by 2. In the flowchart, the True exit of the diamond leads to "even".</details>
<details><summary>5. Sum of N numbers entered by the user</summary><pre>Read N
sum ← 0, count ← 0
while count &lt; N
    Read Num
    sum ← sum + Num
    count ← count + 1
Print sum</pre></details>
<details><summary>6. LCM of two numbers</summary>Use the greatest common divisor (GCD) by repeated remainders:<pre>Read M, N
A ← M, B ← N
while N &gt; 0
    Temp ← M % N
    M ← N
    N ← Temp
GCD ← M
LCM ← A * B / GCD
Print LCM</pre>Trace it with M = 12, N = 8: the loop gives (8, 4), then (4, 0), so GCD = 4 and LCM = 12 * 8 / 4 = 24.</details>

<h2 id="langs">6. Programming languages</h2>
<p>A programming language is an artificial language used to control a computer. Like natural languages, it is defined by syntactic and semantic rules. <b>Low-level:</b> machine and assembly. <b>High-level:</b> C, C++, Java.</p>
<div class="tw"><table><tr><th>Gen.</th><th>Type</th><th>Traits</th></tr>
<tr><td>1st</td><td>Machine language</td><td>0s and 1s; long and difficult</td></tr>
<tr><td>2nd</td><td>Assembly language</td><td>Assembles repetitive instructions; shorter code</td></tr>
<tr><td>3rd</td><td>Procedural</td><td>Include commands; shorter code</td></tr>
<tr><td>4th</td><td>Nonprocedural</td><td>Application generators; commands specify results</td></tr>
<tr><td>5th</td><td>Intelligent</td><td>Natural-language style</td></tr></table></div>
<p style="color:var(--mu)">Progress runs from machine-oriented to human-oriented language. There are over 2,400 programming languages.</p>

<h3>The five generations in more detail</h3>
<details><summary>1st generation: machine language (1940s)</summary>The only language a computer understands directly. Each instruction is zeros and ones, made of an <b>op code</b> (what to do) and an <b>address</b> (where the data is). It is fast and memory-efficient and gives full control of the hardware, but it is very hard to write, and it differs on every type of computer.</details>
<details><summary>2nd generation: assembly language (early 1950s)</summary>Uses short symbols (mnemonics) such as ADD or LOAD instead of binary. A program called an <b>assembler</b> translates it to machine code. It is easier than binary but is still machine-dependent and not portable, and it is used mainly in system software.</details>
<details><summary>3rd generation: high-level languages (1950s to 1970s)</summary>English-like and independent of the machine, so the same program can run on different computers with little change. You can write statements like Z = A + B. Programs must be translated to machine code before running. These are <b>procedural</b>: you state both what to do and how. Examples: C++, FORTRAN, COBOL, BASIC.</details>
<details><summary>4th generation (since late 1970s)</summary>Simple, application-oriented and <b>non-procedural</b>: you say what result you want, not the steps. Easier to write, but you have less control. Examples: SQL, report generators, application generators.</details>
<details><summary>5th generation (1990s)</summary>Close to human speech and used in artificial intelligence and expert systems, for example asking for a customer's sales figure for a given year. They need powerful hardware and software to interpret the commands.</details>
<p style="color:var(--mu)">The higher the level, the easier a language is for people. Machine and assembly languages depend on the computer. High-level languages do not.</p>
<div class="tip"><b>In plain words</b>The computer only understands machine language, which is 0s and 1s. Humans write in higher-level languages that are easier to read, and special programs (compilers or interpreters) translate them for the machine. Which language should you pick? For this course, any popular one works: the thinking skills in this chapter apply to all of them. Think of languages as different tools for the same job, like different brands of hammer.</div>
<h2 id="paradigms">7. Programming paradigms</h2>
<p>A paradigm is a style, or "way", of programming. It is not tied to one language, and languages may follow several paradigms.</p>
<div class="tw"><table><tr><th>Paradigm</th><th>Description</th><th>Model</th><th>Examples</th></tr>
<tr><td>Imperative (procedural)</td><td>Statements directly change state</td><td>Algorithms + data</td><td>C, C++, Java, PHP, Python, Ruby</td></tr>
<tr><td>Logical (declarative)</td><td>Defines logic, not control flow</td><td>Facts + rules</td><td>Prolog, SQL, CSS</td></tr>
<tr><td>Functional</td><td>Evaluation of mathematical functions; avoids state</td><td>Functions of functions</td><td>C++, Lisp, Python, JavaScript</td></tr>
<tr><td>Object-oriented</td><td>Objects manipulated through methods</td><td>Objects + messages</td><td>C++, C#, Java, PHP, Python</td></tr></table></div>

<h3>The paradigms in more detail</h3>
<details><summary>Unstructured (sequential) programming</summary>Commands run in order, usually one per line, and execution can jump to any numbered or labeled line. The whole program is one block, so it is hard to change and debug: a bug means checking everything.</details>
<details><summary>Procedural programming</summary>A <b>procedure</b> (also called routine, subroutine, method or function) is a named set of steps you can call from anywhere. After it finishes, control returns to where it was called. Benefits: reuse of the same code without copying, easier tracking than GO TO jumps (which can create tangled spaghetti code), and easier error-finding because a procedure that is correct stays correct. Examples: C, Pascal, FORTRAN.</details>
<details><summary>Modular (structured) programming</summary>A discipline within procedural programming. Procedures with a common purpose are grouped into <b>modules</b>, each of which can be written and tested on its own. <b>Scoping</b> stops one procedure from touching another's variables, which keeps modules independent.</details>
<details><summary>Functional programming</summary>Computation is the evaluation of mathematical functions. Values are not changed; they are turned into new values. The same input always gives the same output, with no side effects, and recursion is common. Examples: Lisp, Scheme.</details>
<details><summary>Logic programming</summary>You state facts and rules, and the system works out the answers. Example in Prolog: brother(X,Y) is true if X and Y have the same father F and the same mother M, and X is male.<pre>brother(X,Y) :- father(F,X), father(F,Y),
                mother(M,X), mother(M,Y), male(X).</pre></details>
<details><summary>Object-oriented programming (OOP)</summary>A program is a collection of cooperating <b>objects</b>. Each object bundles its data with the functions that work on it (<b>encapsulation</b>), and objects interact by sending messages. Benefits: reuse through inheritance, data hiding, and easy mapping of real-world things to program parts. Examples: Java, C++, Smalltalk.</details>
<div class="tw"><table><tr><th>Procedure-oriented (POP)</th><th>Object-oriented (OOP)</th></tr>
<tr><td>Program divided into procedures</td><td>Program divided into objects</td></tr>
<tr><td>Global data shared by many functions</td><td>Data tied to the functions that use it and protected</td></tr>
<tr><td>Data moves freely between functions</td><td>Data is hidden</td></tr>
<tr><td>Hard to add new data and functions</td><td>Easy to add new data and functions</td></tr>
<tr><td>Top-down approach</td><td>Bottom-up approach</td></tr></table></div>
<div class="tip"><b>In plain words</b>Paradigms are different styles of giving instructions. <b>Imperative:</b> you tell the computer exactly what to do, step by step, like a recipe. <b>Logical or declarative:</b> you state what you want, and the system works out how (a database query asks for what you want, not how to search). <b>Functional:</b> you build the result by combining small functions, like a chain of calculators. <b>Object-oriented:</b> you model things as objects that hold data and can do actions, such as a Student object with a name and a method to enroll. You do not need to master these now. Just know they exist, because you will meet them in later courses.</div>
<h2>Summary</h2>
<p>You practiced analyzing problems, writing pseudocode, and constructing flowcharts to turn computational problems into solutions.</p>
<h2 id="gloss">Glossary for beginners</h2>
<dl><dt>Source code</dt><dd>The text of a program, written by a programmer.</dd><dt>Debugging</dt><dd>Finding and fixing mistakes (bugs) in a program.</dd><dt>Stakeholder</dt><dd>Anyone affected by or interested in the software, such as users, clients and managers.</dd><dt>Variable</dt><dd>A named place that stores a value, such as sum or counter.</dd><dt>Initialize</dt><dd>Give a variable its starting value.</dd><dt>Loop</dt><dd>A set of steps that repeats while a condition is true.</dd><dt>Syntax</dt><dd>The spelling and grammar rules of a language.</dd><dt>Semantics</dt><dd>What a statement means or does.</dd><dt>Feasibility study</dt><dd>An early check of whether a project is worth doing (organizational, economic, technical, operational).</dd><dt>Pseudocode</dt><dd>An informal, language-independent way to write an algorithm in plain steps.</dd><dt>Procedure (function)</dt><dd>A named set of steps you can run from anywhere in a program.</dd><dt>Module</dt><dd>A group of related procedures that can be written and tested separately.</dd><dt>Encapsulation</dt><dd>Keeping data and the functions that use it together inside an object, hidden from outside.</dd><dt>Top-down / bottom-up</dt><dd>Splitting a big problem into parts, or building a solution from the smallest parts.</dd><dt>Heuristic</dt><dd>A rule of thumb or guess. Computers need exact steps, not guesses.</dd></dl>
<h2>Self-check questions</h2>
<details><summary>1. What three questions define a problem in problem analysis?</summary>Input (what data do we have), process (how do we get from the data to the result), output (what result is required).</details>
<details><summary>2. Name two characteristics of a good algorithm.</summary>Any two of: definiteness, finiteness, input, output, effectiveness. For example, it must be clear, and it must end.</details>
<details><summary>3. When would you use a diamond in a flowchart?</summary>For a decision: a yes/no question where the flow goes one of two ways.</details>
<details><summary>4. Is Python a low-level or high-level language?</summary>High-level. Machine and assembly languages are low-level.</details>
<details><summary>5. Why analyze a problem before coding?</summary>To understand what is really needed and to check the solution idea before spending time building it.</details>
<details><summary>6. What is the difference between a system flowchart and a program flowchart?</summary>A system flowchart shows the overall logic of a data-processing system. A program flowchart shows the operations and decisions inside one program.</details>
<details><summary>7. Write the steps to swap the contents of two cups of liquid.</summary>Use a third, empty cup. 1. Pour cup A into cup C. 2. Rinse cup A. 3. Pour cup B into cup A. 4. Rinse cup B. 5. Pour cup C into cup B. The third cup works like a temporary variable (temp) when you swap two values in a program.</details>
<details><summary>8. Name the four parts of a loop.</summary>Initialization, computation, test and update.</details>
<details><summary>9. Which approach splits a problem down, and which merges parts up?</summary>Top-down splits a big problem into smaller parts. Bottom-up solves the smallest parts first and merges them.</details>
<details><summary>10. Practice: write steps to count how many times the letter e appears in a sentence.</summary>Set count ← 0. For each letter in the sentence: if the letter is e, then count ← count + 1. When the letters run out, print count. Also try: find the first occurrence of the name JEAN in a list of names, and think about how an alphabetical list would let you stop earlier.</details>
<h2 id="refs">Reading resources</h2>
<ul><li>Savitch, <i>Problem Solving with C++</i>, 10th ed., 2018 (Chapters 1–3).</li><li>Zak, <i>An Introduction to Programming with C++</i>, 8th ed., Cengage, 2016 (Chapters 2–3).</li></ul>
</main>
<footer>Fundamentals of Programming I · Chapter 1</footer>
</body></html>
