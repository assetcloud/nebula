# Delete Vertex Syntax

Nebula 支持给定一个 vertex Id，删掉这个顶点和与它相关联的入边和出边，语法如下：

```sql
DELETE VERTEX $vid
```

系统内部会找出这个与顶点相关联的出边和入边，把他们全部删除成功后，最后删除点相关的信息。整个过程当前还无法保证原子性，因此当遇到失败时请重试。