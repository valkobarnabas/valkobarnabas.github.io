# Visualizing Irreducible $T$-modules for Distance-Regular Graphs

## Overview
This project is an interactive web-based visualization tool that serves as supplementary material for the mathematical paper **"The Terwilliger algebra for the distance-regular graphs with valency three."** It was developed as part of a project for the Madison Experimental Mathematics Laboratory (MXM) at the University of Wisconsin–Madison (Academic Year 2025/26).

By a classical theorem, there are exactly 13 distance-regular graphs of valency three. The accompanying paper gives an orthogonal direct-sum decomposition of the standard module $V = \mathbb{C}^X$ into irreducible $T$-modules for each of these graphs, providing an explicit pure basis for each module. 

This visualization makes these decompositions visually clear. Users can select any of the 13 graphs and their corresponding $T$-modules, load an initial basis vector, and interactively verify its closure under the adjacency matrix $A$.

## How It Works
The standard module $V = \mathbb{C}^X$ associated with a distance-regular graph decomposes into an orthogonal direct sum of irreducible $T$-modules. This tool allows you to:
1. **Select a Graph & $T$-module:** Choose one of the 13 graphs and a specific irreducible module.
2. **Choose an Initial Basis Vector:** Load a starting basis vector $\mathbf{v}_i$ onto the graph's vertices.
3. **Apply Adjacency Matrix $A$:** Clicking the "Apply Adjacency Matrix $A$" button updates each vertex's value to the sum of its neighbors' current values.
4. **Observe Closure:** The visualization dynamically demonstrates that the resulting vector remains entirely within the span of the module's basis, proving closure under $A$.

## Features
* **Interactive Graph Rendering:** Built with D3.js, the nodes and edges smoothly animate to reflect mathematical operations.
* **Color Mapping:** Each basis vector is assigned a distinct color. When $A$ is applied, vertices containing contributions from multiple basis vectors visually split into multiple colors.
* **Live Linear Combinations:** The current vector state is mathematically rendered using MathJax at the bottom of the screen.
* **Real-time Matrix Tracking:** The matrix representation of $A$ in the selected basis is displayed, highlighting the corresponding column when a vector is acted upon.
* **Subconstituent Highlights:** Explore subconstituents $\Gamma_i$ visually by hovering over the distance partitions table.
* **Data Downloads:** Users can download the Adjacency matrix $A$ (.txt) and the dual primitive idempotents $\{E_i^*\}_{i=0}^D$ (.zip) for all 13 graphs to verify basis vector transformations in your choice of software.

## Included Graphs
The `t_modules.json` dataset contains pre-calculated vertex, edge, layout, and $T$-module basis data for all 13 distance-regular graphs with valency three:
1. $K_4$
2. $K_{3,3}$
3. Petersen Graph
4. 3-cube
5. Heawood Graph
6. Pappus Graph
7. Coxeter Graph
8. Tutte's 8-cage
9. Dodecahedron
10. Desargues Graph
11. Tutte's 12-cage (both $x \in X^+$ and $x \in X^-$ cases)
12. Biggs-Smith Graph
13. Foster Graph

## Project Link
This webpage can be viewed live at [valkobarnabas.github.io/tmodules](valkobarnabas.github.io/tmodules).

## Technologies Used
HTML/CSS/Vanilla JS: Core structure and styling.

D3.js (v7.9): SVG graph rendering, node/link physics, and interactive animations.

MathJax (v3): LaTeX equation rendering for vectors and matrices.

math.js (v11.8): Linear algebra and matrix operations under the hood.

JSZip (v3.10): Client-side generation of .zip files for matrix downloads.

## Credits
This project was headed by Professor Paul Terwilliger, with undergraduate contributors Kevin Kauflin, Barnabás Valkó, and Hanyi Wu. The graduate mentor for the project was Jimmy Vineyard.

This website and the data user herein was designed and derived by Barnabás Valkó (UW–Madison Mathematics and Statistics, B.S. 2027). Please feel free to address feedback to [bvalko(at)wisc(dot)edu](mailto:bvalko@wisc.edu).

Many of the calculations in this paper were performed using the R programming language. The graph layouts were generated using R along with data from Wikipedia.
