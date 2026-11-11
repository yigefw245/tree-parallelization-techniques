# k-d 树（k-d tree）

k-d 树是一种组织 k 维点的二叉空间索引。每个分割节点选择一个坐标轴和一个分割值，把当前区域划成两部分。构建时可以沿所选轴取中位数，让两侧的点数接近。

k-d 树常用于低维点集的范围搜索和最近邻查询。例如在点云中查找距离某个点最近的点时，可以跳过与查询点的最小可能距离已经超过当前最优距离的子区域。

## 实现分类

- [构造](build/)涵盖选取分割轴和分割值，再并行构建两侧子树。
- [查询](query/)涵盖处理范围搜索、最近邻搜索或多点批量查询。
- [重建](rebuild/)涵盖点集变化造成树失衡后，重新划分受影响的子树。

更多细节见 [Jon Louis Bentley, Multidimensional Binary Search Trees Used for Associative Searching](https://cs.wmich.edu/gupta/teaching/cs6310/lectureNotes_cs6310/kdtree-bentley.pdf)
