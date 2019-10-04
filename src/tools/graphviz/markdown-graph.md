---
markdown:
  image_dir: /assets/graphviz
  path: /tools/graph-tool/graphviz/markdown-graph.md
  absolute_image_path: true
---

## plantuml

```puml {filename="graphviz-markdown-plantuml.png"}
@startuml
A -> B
@enduml
```

## graphviz

### Simple Graph

```dot {filename="graphviz-simple-graph.png"}
graph {
    a -- b;
    b -- c;
    a -- c;
    d -- c;
    e -- c;
    e -- a;
}
```

### Graph Direction

```dot {filename="graphviz-graph-direction.png"}
graph {
  rankdir=LR;
  a -- b;
  b -- c;
  a -- c;
  d -- c;
  e -- c;
  e -- a;
}
```

### Simple Digraph (有向图)

```dot {filename="graphviz-simple-digraph.png" engine="neato"}
digraph {
    a -> b;
    b -> c;
    c -> d;
    d -> a;
}
```

### Full Digraph

```dot {filename="graphviz-full-digraph.png"}
digraph {
    a -> b[label="0.2",weight="0.2"];
    a -> c[label="0.4",weight="0.4"];
    c -> b[label="0.6",weight="0.6"];
    c -> e[label="0.6",weight="0.6"];
    e -> e[label="0.1",weight="0.1"];
    e -> b[label="0.7",weight="0.7"];
}
```

### Style Path

```dot {filename="graphviz-style-path.png"}
graph {
    a -- b[color=red,penwidth=3.0];
    b -- c;
    c -- d[color=red,penwidth=3.0];
    d -- e;
    e -- f;
    a -- d;
    b -- d[color=red,penwidth=3.0];
    c -- f[color=red,penwidth=3.0];
}
```

#### shorthand of styling path

```dot {filename="graphviz-style-path-shorthand.png"}
graph {
    a -- b -- d -- c -- f[color=red,penwidth=3.0];
    b -- c;
    d -- e;
    e -- f;
    a -- d;
}
```

### Subgraph

```dot {filename="graphviz-subgraph.png"}
digraph {
    subgraph cluster_0 {
        label="Subgraph A";
        a -> b;
        b -> c;
        c -> d;
    }

    subgraph cluster_1 {
        label="Subgraph B";
        a -> f;
        f -> c;
    }
}
```

#### seperate nodes and edges expression of subgraph

```dot {filename="graphviz-subgraph-seperate-node-edge.png"}
graph {
  splines=line;
  subgraph cluster_0 {
    label="Subgraph A";
    a;b;c;
  }
  subgraph cluster_1 {
    label="Subgraph B";
    d;e;f;
  }
  a--d
  b--d
  b--e
  c--e
  c--f
  f--a
}
```

### Big Graph Tricks

- 通过{}能用一个语句组织图的多个边
- 通过`rank`来组织节点的层级结构

```dot {filename="graphviz-big-graph-tricks.png"}
graph {
  rankdir=LR;
  a -- { b c d }; b -- { c e }; c -- { e f }; d -- { f g }; e -- h;
  f -- { h i j g }; g -- k; h -- { o l }; i -- { l m j }; j -- { m n k };
  k -- { n r }; l -- { o m }; m -- { o p n }; n -- { q r };
  o -- { s p }; p -- { s t q }; q -- { t r }; r -- t; s -- z; t -- z;
  { rank=same; b, c, d }
  { rank=same; e, f, g }
  { rank=same; h, i, j, k }
  { rank=same; l, m, n }
  { rank=same; o, p, q, r }
  { rank=same; s, t }
}
```
