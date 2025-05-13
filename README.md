# cs221-project-2-n-queens-solved
**TO GET THIS SOLUTION VISIT:** [CS221 Project 2-N-Queens Solved](https://www.ankitcodinghub.com/product/cs221-project-2-n-queens-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;93534&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS221 Project 2-N-Queens Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
CSP for N-Queens

</div>
</div>
<div class="layoutArea">
<div class="column">
A basic backtracking search BacktrackingSearch is already implemented in submission.py. The function will help you solve the CSP. You should read it carefully to make sure that you understand how the backtracking search is working.

</div>
</div>
<div class="layoutArea">
<div class="column">
a)

</div>
<div class="column">
&nbsp;Let’s create a CSP to solve the N-Queens problem: Given an 𝑛×𝑛 board, we’d like to place 𝑛 queens on this board such that no 2 queens are on the same row, column, or diagonal. Implement create_n_queens_csp() by adding n variables and some number of binary factors. Note that the solver collects some basic statistics on the performance of the algorithm. You should take advantage of these statistics for debugging and analysis. You should get 92 (optimal) assignments for 𝑛 = 8 with exactly 2057 operations (number of calls to backtrack()).

Hint: If you get a larger number of operations, make sure your CSP is minimal. Try to define the variables such that the size of domain is O(n).

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
<ol start="2">
<li>b) &nbsp;[5 points] You might notice that our search algorithm explores quite a large number of states even
for the 8×8 board. Let’s see if we can do better. One heuristic we discussed in class is using most

constrained variable (MCV): To choose an unassigned variable, pick the 𝑋 that has the fewest &amp;

number of values 𝑎 which are consistent with the current partial assignment (𝑎 for which check_factor() on 𝑋 = 𝑎 returns True). Implement this heuristic in get_unassigned_variable()

under the condition self.mcv = True. It should take you exactly 1361 operations to find all optimal assignments for 8 queens CSP — that’s 30% fewer!

Some useful fields:

Ø csp.unary_factors[var][val] gives the unary factor value.

Ø csp.binary_factors[var1][var2][val1][val2] gives the binary factor value.

2 Here, var1 and var2 are variables and val1 and val2 are their corresponding values.

Ø In BacktrackingSearch, if var has been assigned a value, you can retrieve it using

assignment[var]. Otherwise var is not in assignment.
</li>
<li>c) &nbsp;[10 points] The previous heuristics looked only at the local effects of a variable or value. Let’s now
implement arc consistency (AC-3) that we discussed in lecture. After we set variable 𝑋 to value &amp;

𝑎, we remove the values 𝑏 of all neighboring variables 𝑋) that could cause arc-inconsistencies. If 𝑋)’s domain has changed, we use 𝑋)’s domain to remove values from the domains of its neighboring variables. This is repeated until no domains have changed. Note that this may significantly reduce your branching factor, although at some cost. In backtrack() we’ve implemented code which copies and restores domains for you. Your job is to fill in arc_consistency_check().

With AC-3 enabled, it should take you 769 operations only to find all optimal assignments to 8 queens CSP — That is almost 45% fewer even compared with MCV!

Take a deep breath! This part requires time and effort to implement — be patient.

Hint 1: documentation for CSP.add_unary_factor() and CSP.add_binary_factor() can be helpful. Hint 2: although AC-3 works recursively, you may implement it iteratively. Using a queue might be a good idea. li.pop(0) removes and returns the first element for a python list li.
</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
&nbsp;

</div>
</div>
</div>
