# LL1 Parsing
The Objective of The Program: 

1- an	attempt	to	find	a	leftmost	derivation	for	an	
input	string.

2- an	attempt	to	construct	a	parse	tree	for	the	input	
string	starting	from	the	root	and	creating	the	nodes	
of	the	parse	tree	in	preorder.

How Does It Work?

Step 1: First check for left recursion in the grammar, if there is left recursion in the grammar 
remove that and go to step 2.

Step 2: Calculate First() and Follow() for all non-terminals.
First(): If there is a variable, and from that variable, if we try to drive all the strings then the 
beginning Terminal Symbol is called the First.
Follow(): What is the Terminal Symbol which follows a variable in the process of derivation.

Step 3: For each production A –> α. (A tends to alpha)
-Find First(α) and for each terminal in First(α), make entry A –> α in the table.
-If First(α) contains ε (epsilon) as terminal than, find the Follow(A) and for each terminal in 
Follow(A), make entry A –> α in the table.
-If the First(α) contains ε and Follow(A) contains $ as terminal, then make entry A –> α in the 
table for the $.
