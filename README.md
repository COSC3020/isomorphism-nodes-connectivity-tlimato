# Isomorphism

Prove that if two graphs $A$ and $B$ have the same number of nodes and are
completely connected, they must be isomorphic. I have started with the formal
definition of isomorphism below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.

## Answer
Let $A = (V_A, E_A)$ and $B = (V_B, E_B)$ be two completely connected graphs. Additionally, both graphs have the same number of nodes, say $n$.
Let's also recall that a graph is completely connected (or complete) if there is an edge between every pair of distinct vertices.

### Proof
1. **Cardinality**: Since both $A$ and $B$ have $n$ nodes, then lets say sets $V_A$ and $V_B$ both have cardinality $n$.

2. **Edge Set Construction in Complete Graphs**:
In a complete graph with  $n$ vertices, every pair of distinct vertices is connected by a unique edge. Since each vertice can connect to every other vertice exactly once, the total number of edges is the amount of all possible pairs of vertices.
For each vertice, you can pair it with any of the remaining  $n-1$ vertices. However, this method counts each edge twice  (once for each vertice in the edge), so the total number of edges is half the product of  $n$ and  $n-1$. Therefore, the number of edges in a complete graph is  $\frac{n(n-1)}{2}$. 
We can then state that  $|E_A|  =  |E_B|  =  \frac{n(n-1)}{2}$.

3. **Showing  a Bijection**:
Since  $|V_A|  =  |V_B|  = n$, there exists a bijection  $f: V_A  \rightarrow V_B$ that is possible because both sets of vertices have the same finite number of elements. By definition of isomorphism, this bijection  $f$ must satisfy the condition that  $(u,v)  \in E_A$ if and only if  $(f(u),f(v))  \in E_B$, applying for all arbitrary  $u$ and  $v$, with their corresponding  $f(u)$ and  $f(v)$, as outlined by the one-to-one and onto properties of a bijection.

4. **Edge Relations remain Intact**:
- In $A$, every pair of distinct vertices $(u, v) \in V_A$ is connected, so $(u, v) \in E_A$.
   
- Since $f$ is a bijection, and $B$ is also a complete graph, for every $(u, v) \in E_A$, the vertices $f(u)$ and $f(v)$ are distinct and $(f(u), f(v)) \in E_B$.
- Conversely, if $(f(u), f(v)) \in E_B$, then $(u, v) \in E_A$ because $f$ is a bijection and maps every pair of distinct vertices in $V_A$ to a pair of distinct vertices in $V_B$.

6. **Conclusion**:
- The function $f$ is a bijection such that $(u, v) \in E_A$ if and only if $(f(u), f(v)) \in E_B$.
- Therefore, by the definition of graph isomorphism, $A$ is isomorphic to $B$. This means any two completely connected graphs with the same cardinality (same number of Nodes) are Isomorphic, as there always exists a bijection between their sets of vertices that preserves the adjacency relation.
