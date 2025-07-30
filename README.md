# Tree-Models-Library
3D models of fruit trees used for robot task-based optimization.

Created by Victor Bloch, Amir Degani, Avital Bechar.

The library includes about 20 detailed tree models of actual trees in orchards. The models consist of a list of geometric primitives modeling the tree branches and fruit. MATLAB functions for reading the models are also provided.
The tree models data is stored in .txt files in Tree Models folder.
The MATLAB function TreeRead.m is used to read the .txt files. The function DrawTree.m is used to draw the tree model.
The explanation about the tree models, data structure, and MATLAB functions is given in Tree Model Library Explanation.pdf.

## Pickle files
For each tree files `TreeModels/tree.txt`, `TreeModels/tree.pkl` contains a dictionary
```python
data = {
    "tree": {
        "BranchN": ...,
        "BranchPos": ...,
        "BranchVec": ...,
        "BranchR": ...,
        "FruitN": ...,
        "FruitPos": ...,
        "FruitR": ...,
    },
    "target_poses": List[SE3],
    "not_reachables": List[int],
}
```

The list of `SE3` targets, `target_poses`, is generated for a specific end-effector collision model, and quaternion clustering.

