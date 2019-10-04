  
  
##  plantuml
  
  

![](/assets/graphviz/graphviz-markdown-plantuml.png?0.45741585705065835)  
  
##  graphviz
  
  
###  Simple Graph
  
  

![](/assets/graphviz/graphviz-simple-graph.png?0.337476206483027)  
  
###  Graph Direction
  
  

![](/assets/graphviz/graphviz-graph-direction.png?0.7987390852001437)  
  
###  Simple Digraph (有向图)
  
  

![](/assets/graphviz/graphviz-simple-digraph.png?0.4494015511448295)  
  
###  Full Digraph
  
  

![](/assets/graphviz/graphviz-full-digraph.png?0.35402721500820755)  
  
###  Style Path
  
  

![](/assets/graphviz/graphviz-style-path.png?0.8053743387438297)  
  
####  shorthand of styling path
  
  

![](/assets/graphviz/graphviz-style-path-shorthand.png?0.7401996548948846)  
  
###  Subgraph
  
  

![](/assets/graphviz/graphviz-subgraph.png?0.40450309158904885)  
  
####  seperate nodes and edges expression of subgraph
  
  

![](/assets/graphviz/graphviz-subgraph-seperate-node-edge.png?0.5444716415776609)  
  
###  Big Graph Tricks
  
  
- 通过{}能用一个语句组织图的多个边
- 通过`rank`来组织节点的层级结构
  

![](/assets/graphviz/graphviz-big-graph-tricks.png?0.20441634632945616)  
  
##  Ditta
  
  
```ditaa {code_chunk_offset=0, filename="ditta.png" cmd=true args=["-E"]}
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
  
![](/assets/ditta.png )
  