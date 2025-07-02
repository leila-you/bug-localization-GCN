# bug-localization-GCN
Here are the project execution steps :


---
The dataset used in this project is available at the following link: https://github.com/AI-nstein/hoppity

1. Converting Code to AST Graph

For JavaScript code:
  Use tools available in the [Hoppity repository](https://github.com/AI-nstein/hoppity) to convert JavaScript code into AST trees, which serve as the basis for graph construction.
For Python code:
  Use the `py_to_ast` tool to convert Python code into Abstract Syntax Tree (AST) graphs.

---

2. Running GumTree Tool

* The GumTree algorithm extracts the differences between two versions of code.
* The output includes operations such as `insert`, `delete`, `update`, and `move` on graph nodes.

---

 3. Node Labeling Based on GumTree Output

* Each graph node is labeled according to the changes identified by GumTree.
* Labels include categories like `added`, `deleted`, `updated`, and `unchanged`.
 Use the `labeling nodes based on gumtree results` code
---

 4. Applying GraphSMOTE

* To address class imbalance in the graph data, an oversampling method called GraphSMOTE is applied.
* This method generates synthetic samples to enhance minority classes.
Use the `GraphSMOTE_imbalanced` code
---

5. Running GCN Model for Node Classification

* A deep learning model, Graph Convolutional Network (GCN), is run on the graphs.
* Using node features and graph structure, the model predicts the final label of each node.
 Use the `node_classification_gcn` code

