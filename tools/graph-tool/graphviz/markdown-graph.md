  
  
##  plantuml
  
  

![](/assets/graphviz/graphviz-markdown-plantuml.png?0.5228200270208556)  
  
##  graphviz
  
  
###  Simple Graph
  
  

![](/assets/graphviz/graphviz-simple-graph.png?0.12889704142127445)  
  
###  Graph Direction
  
  

![](/assets/graphviz/graphviz-graph-direction.png?0.0584088194901351)  
  
###  Simple Digraph (有向图)
  
  

![](/assets/graphviz/graphviz-simple-digraph.png?0.24086648886526119)  
  
###  Full Digraph
  
  

![](/assets/graphviz/graphviz-full-digraph.png?0.7207719536461943)  
  
###  Style Path
  
  

![](/assets/graphviz/graphviz-style-path.png?0.7186793838800449)  
  
####  shorthand of styling path
  
  

![](/assets/graphviz/graphviz-style-path-shorthand.png?0.459157702726698)  
  
###  Subgraph
  
  

![](/assets/graphviz/graphviz-subgraph.png?0.16013929105641522)  
  
####  seperate nodes and edges expression of subgraph
  
  

![](/assets/graphviz/graphviz-subgraph-seperate-node-edge.png?0.4814407641270291)  
  
###  Big Graph Tricks
  
  
- 通过{}能用一个语句组织图的多个边
- 通过`rank`来组织节点的层级结构
  

![](/assets/graphviz/graphviz-big-graph-tricks.png?0.894862676064041)  
  
##  Ditta
  
  
```ditaa {code_chunk_offset=0, cmd=true args=["-E"] filename="graphviz-ditta.png"}
 +--------+   +-------+    +-------+
 |        | --+ ditaa +--> |       |
 |  Text  |   +-------+    |diagram|
 |Document|   |!magic!|    |       |
 |     {d}|   |       |    |       |
 +---+----+   +-------+    +-------+
     :                         ^
     |       Lots of work      |
     +-------------------------+
```
  