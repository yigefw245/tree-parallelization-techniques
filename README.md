# tree-parallelization-techniques

本仓库收集不同树结构的并行化实现，按树结构和操作类型组织。

## 目录结构

| 树结构 | 构造 | 查询 | 重建 |
| --- | --- | --- | --- |
| B 树 | [build](B-tree/build/) | [query](B-tree/query/) | [rebuild](B-tree/rebuild/) |
| B+ 树 | [build](B%2Btree/build/) | [query](B%2Btree/query/) | [rebuild](B%2Btree/rebuild/) |
| 八叉树 | [build](Octree/build/) | [query](Octree/query/) | [rebuild](Octree/rebuild/) |
| R 树 | [build](R-tree/build/) | [query](R-tree/query/) | [rebuild](R-tree/rebuild/) |
| k-d 树 | [build](kd-tree/build/) | [query](kd-tree/query/) | [rebuild](kd-tree/rebuild/) |
| 四叉树 | [build](quadtree/build/) | [query](quadtree/query/) | [rebuild](quadtree/rebuild/) |

- `build/` 收录从输入数据构造树的实现。
- `query/` 收录在现有树上执行查询的实现，例如范围查询和最近邻查询。
- `rebuild/` 收录对已有树进行重建或重新平衡的实现。

## 如何提交贡献

1. 在 GitHub 上 Fork 本仓库，从 `main` 创建一个分支，例如 `kd-tree-range-query`。
2. 按树结构和操作类型放置代码。同一目录可以收录多种实现，建议为自己的实现单独建一个子目录，例如 `kd-tree/query/parallel-range-query/`。
3. 在实现目录里附上 `README.md`，说明算法、并行化方式、依赖以及编译和运行命令，并提供一个可复现的示例。若提交包含性能对比，请注明测试环境、数据规模、线程数和串行基线。
4. 提交并推送到你的 Fork，然后向本仓库的 `main` 分支发起 Pull Request（PR）。在 PR 中写明树结构、操作类型、实现思路和验证结果。一次 PR 建议聚焦一项实现或一组相关改动。
