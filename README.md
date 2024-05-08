[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/ppBU16qM)
# Isomorphism

Prove that if two graphs $A$ and $B$ have the same number of nodes and are
completely connected, they must be isomorphic. I have started with the formal
definition of isomorphism below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.


## Solution
Similar to the Other Isomorphism Problem I just read back up on my Notes, re-referenced the definition of Complete Graphs, and rewrote the entire proof. I apologize it took this long for me to get it right but it's too late for that now.

**Implications of Complete Graph**
First, let's look at the Definition of a complete graph and then we can deduce the implications for 2 Graphs with the same number of Nodes with this property.

- A Graph is complete or in other words, fully connected if there exists a edge between every distinct pair of nodes in the graph.

Therefore if a graph has $n$ nodes, it must have $n(n-1)/2$ edges, as is derived from the combination of any 2 nodes, such that each is connected to every other node exactly once.

Given we know that both $A$ and $B$ have the same number of nodes and are fully connected, we can deduce that they must also have the same number of edges.
Using this fact we can categorize the Properties of A and B.

- Given $A$ & $B$ have the same number of nodes, let's denote  the number of nodes in both as $n$

- Meaning for $A = [V_A, E_A]$, $V_A = [{a_0, a_1, \ldots, a_n}]$.
- And for $B = [V_B, E_B]$, $V_B = [{b_0,  b_1, \ldots, b_n}]$

Subsequently, we can deduce that $|E_A| = |E_B| = \frac{n(n-1)}{2}$

**Bijection Definition**
For $A$ & $B$ to be isomorphic, we need to find a bijection:

$$
f: V_A \rightarrow V_B \text{ such that every } a_i \text{ from } a_0 \text{ to } a_n \text{ in } V_A \text{ is mapped to a unique } b_j \text{ from } b_0 \text{ to } b_n \text{ in } V_B.
$$

Furthermore, we need to make sure that all the edges that makeup $E_A$ are also present in $E_B$ through the bijection.

**Bijection Exists**
For us to fulfill a bijection, function f must exist and be one-to-one and onto. 
A one-to-one function exists, if there are distinct nodes from $V_A$ that map to distinct nodes that are in $V_B$. This makes sure we can't map multiple nodes from graph $A$ to a distinct node in $B$

Additionally, an onto function exists if its possible to link all of the nodes in $V_B$ back to a given node in $V_A$. 
Because both graphs $A$ and $B$ share the same number of nodes $n$ it's possible to map nodes from  $V_A$ to a given node in $V_B$ using a one-to-one function.
Furthermore, because both graphs are fully connected and have the same number of $n$ nodes there will be $n-1$ edges from each node, connecting to the rest of the nodes in the Graph. ( $n-1$ because we aren't worried about total combinations which is used to find the amount of edges in each Graph with $n$ nodes)

Because every node is connected to every other node, each node from $A$ can be mapped to a unique node in $B$. Because the Graphs are fully connected it doesn't matter which node in $A$ you map to $B$ using an onto-function, the edges will be preserved as $f:V_A \rightarrow V_B$ because they are both fully connected.

Therefore, any random mapping of vertices would be a one-to-one and onto function as no more than 1 distinct node in $A$ would map to any given Node in $B$, and any node in $B$ can be traced back to $A$ and as a result a bijection $f: V_A \rightarrow V_B$ such that $(a_x, a_y))
\in E_1$ iff $(f(a_x),f(a_y)) \in E_2$ must exist.

**Implications of a Bijection Existing**
Well, Given A & B are complete Graphs, every 2 distinct nodes in either set of nodes form an edge in $E_A$ and $E_B$.
Thus, for any 2 nodes in $V_A$, $a_x$ and $a_y$, there exists an edge $(a_x, a_y) \in E_A$. 
The same is true for $E_B$, for any 2 nodes in $V_B$, $b_x$ and $b_y$, there exists an edge $(b_x, b_y) \in E_B$.

Given f: $V_A \rightarrow V_B$ is a bijection [is one-to-one and onto], we can deduce that $f(a_x) = b_y$ and $f(a_y) = b_x$ for all $a_x$ and $a_y$ in $V_A$.
Thus, for any edge $(a_x, a_y) \in E_A$, there exists a corresponding edge $(b_x, b_y) \in E_B$ as their number of nodes and edges are the same.
This means that, f: $V_A \rightarrow V_B$  such that  $(a_x, a_y) \in E_A$, if  $(f(a_x), f(a_y)) \in E_B$.

**Conclusion** 
As both $A$ & $B$ are complete Graphs, and have the same number of nodes, and there exists a bijection $f: V_A \rightarrow V_B$ such that $(a_x, a_y) \in E_A$, if  $(f(a_x), f(a_y)) \in E_B$ it follows that by the definition of isomorphism, $A$ & $B$ are isomorphic.

## Citations

I re-reviewed my notes and my previous attempts.
The following source is where I validated and learned a lot about the specifics surrounding Complete Graphs and the implications this property can have when comparing two graphs.
https://mathworld.wolfram.com/CompleteGraph.html

This is where I refreshed myself on the combination formula briefly touched on in Discrete Structures.
https://stilleducation.com/combination-formula/

This helped me immensely to build my explanation of bijection f and why it must exist. I was familiar with these terms from the videos covering isomorphism and from last semester in discrete Structure but this visual explanation helped immensely.
https://www.khanacademy.org/math/linear-algebra/matrix-transformations/inverse-transformations/v/surjective-onto-and-injective-one-to-one-functions

General Disclaimer:
I use Github copilot to assist in writing code, It's built into my vs code install I use for Professional work and It's helpful in accelerating projects and avoiding syntax issues. I will make this clarification on other assignments as well.
