# R 树（R-tree）

R 树是用于空间对象的平衡索引。在二维场景中，叶节点为对象保存最小外接矩形及对象引用，内部节点用外接矩形包住相应子树中的所有对象。同一层的外接矩形可能重叠，查询因此可能需要访问多个分支。

R 树常用于 GIS 和空间数据库。例如查找与一个地图窗口相交的地块时，可以先用外接矩形筛选候选，再检查地块的实际几何形状。

## 实现分类

- [构造](build/)涵盖按对象的空间位置分组，批量装载索引。
- [查询](query/)涵盖处理空间范围或相交查询，并行检查可能命中的分支。
- [重建](rebuild/)涵盖批量更新后重新组织节点，减少外接矩形之间的重叠。

更多细节见 [Antonin Guttman, R-Trees: A Dynamic Index Structure for Spatial Searching](https://www.cs.princeton.edu/courses/archive/fall08/cos597B/papers/rtrees.pdf)
