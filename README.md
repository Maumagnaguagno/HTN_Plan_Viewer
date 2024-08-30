# HTN Plan Viewer
**Graph visualization of HTN plans using IPC output format**

Convert a [HTN IPC plan](https://ipc2020.hierarchical-task.net/data/format.pdf) into a [DOT](https://www.graphviz.org/doc/info/lang.html) graph to be client-rendered using [d3-graphviz](https://github.com/magjac/d3-graphviz).  
Lines that appear before the root top level tasks correspond to the actions from classical plans.
Lines after the root correspond to the method decompositions done to achieve the plan.
The first symbol of each line is an integer reference and not required to match any order, while the rightmost references, applicable only to methods, refer to their decompositions.
The current implementation expects conforming plans, but warns about lines that do not match any of the possible configurations and missing elements.  

Instead of typing or pasting your plan, the URL can contain a plan or load from a file.  
To load from a plan encoded URL:

```
https://maumagnaguagno.github.io/HTN_Plan_Viewer?plan=1%20action1%0A2%20action2%0Aroot%200%0A0%20task%20-%3E%20method%201%202
```

To load from a planner output file, [limited to GitHub](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing):

```
https://maumagnaguagno.github.io/HTN_Plan_Viewer?from=https://maumagnaguagno.github.io/HTN_Plan_Viewer/plan.txt
```

This project is the counterpart of [Classical Plan Viewer](../../../Classical_Plan_Viewer).