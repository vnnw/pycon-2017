# pycon-2017
Mastering scipy.spatial PyCon 2017 Tutorial

## Dependencies
The tutorial is designed to be executed in a single Jupyter (5.0) notebook in Python 3.x (I've been using 3.5 / 3.6 mostly) and the necessary files may be cloned from this github repo. The easiest way to identify any library dependencies you may be missing is probably to try running all cells in the notebook (`Cell` -> `Run All`) and checking if there are any issues. Nonetheless, I've tried to consolidate major import statements near the top of the notebook, and the following is a summary of the versions I've used:

| library import name | version used |
|---------------------|--------------|
| scipy | `0.19.0` |
| numpy | `1.12.1` |
| matplotlib | `2.0.0` |
| PIL | `4.1.0` |
| networkx | `1.11` |

A few other files (image files, small ad hoc Python libraries) are stored in the repo and also needed to run the full notebook.

## Talk Outline

1) Introduction: Computational Geometry and scipy.spatial
2) Distances between arrays of points
    - scipy.spatial.distance_matrix
      - Euclidean (L2 norm)
      - Rectilinear (L1 norm)
    - scipy.spatial.distance.cdist
      - Faster than distance_matrix for Euclidean norm
      - Faster than distance_matrix for L1 norm
      - Using cdist for Mahalanobis distance -- clustering and outlier detection
    - scipy.spatial.distance.pdist
      - pdist basics -- very simple example
      - pdist 'real-world' example
3) Distances between single numeric vectors
    - Calculate the Euclidean distance between two arrays
    - Calculate the cityblock distance between two arrays
    - Calculate the weighted Minkowski distance between two arrays
4) Distances between single boolean vectors
    - Calculate the hamming distance between two 1D arrays
    - Calculate the Jaccard distance between two 1D arrays
    - Calculate the Yule distance (dissimilarity) between two 1D boolean arrays
5) Distances in Large Data Sets: Binary Space Partitioning
    - General Concept of Binary Space Partitioning (BSP)
    - Simple Example of General BSP
    - k-d trees
      - Example Exploring k-d trees with scipy.spatial
6) Convex Hulls
    - Convexity, Convex Hulls and General Position
    - Practical Algorithm Time & Space Complexities
    - Determine the time complexity of the `ConvexHull` algorithm used by `scipy.spatial` (which is actually just a wrapper for the popular `qhull` package)
      -  Can the Python community do better than `scipy.spatial.ConvexHull`?
    - Practical Examples with `scipy.spatial.ConvexHull`
      - 2D
      - 3D
7) Delaunay Triangulations
     - Definition and Basic Information
     - The Empty Circle Property
     - Practical Applications of `scipy.spatial.Delaunay()`
       - 2D
     - Measuring the time complexity of `scipy.spatial.Delaunay()`
8) Voronoi Diagrams
    - Definition and Importance
    - Overview of Algorithms and their Time Complexities (2D)
    - Practical Problem Solving with `scipy.spatial.Voronoi()`
      - 2D
      - 3D
    - Measuring the Time Complexity for 2D `scipy.spatial.Voronoi()`
    - `scipy.spatial.SphericalVoronoi()`
      - Calculating Surface Area of Spherical Polygons
9) Shape Comparison
    - Procrustes analysis
    - Examples using scipy.spatial.procrustes
      - Simple Example -- Two Circles
      - More complex shapes -- comparison of two bone structures
    - The Hausdorff Distance
      - Simple Example: Concentric circles with one outlier
    - The Frechet Distance (Proposed)
      - The Classic / Intuitive Interpretation (Informal Definition)
      - Discrete Frechet Distance Example -- Path of an Autonomous Vehicle
10) Miscellaneous Topics
    - Hyperrectangles
      - Exploring scipy.spatial.Rectangle with some examples
11) Discussion -- What would you really like to have available in scipy.spatial?
      
    
    
