# Review of Linear Algebra

A `Swift` and `Brutal` Introduction to Linear Algebra!

线性代数是计算机图形学的基础。在我看来，使用矩阵表示与运算，很好地利用了图像间的空间特性，也方便硬件对元素进行批量运算，也就加速了渲染速度。

### 向量
讲了：
- 向量
- 向量的乘积 Vector Multiplication
  - 点乘 Dot product ：点乘可以很好地求出夹角，以及用于一个向量到另一个向量的投影（Projection）。
  - 叉乘 Cross product ：可以很好地判断，向量之间的左右关系、点与多边形间的内外关系。

对于`叉乘`而言：
- 遵循右手定则
- $a\times b=-b \times a$
- $||a\times b|| =  ||a||||b||\sin \phi$
- 以下三个表达式等价

$$\vec{a} \times \vec{b}$$

$$A*b$$

$$\begin{pmatrix}
  0& -z_a & y_a\\
  z_a& 0 & -x_a\\
  -y_a& x_a & 0
\end{pmatrix}\begin{pmatrix}
  x_b\\
  y_b\\
  z_a
\end{pmatrix}$$

$A$ is dual matrix of vector a.

### 矩阵
此外，还讲了：
- 正交坐标系 Orthonormal Coordinate Frames
- 矩阵
  - 矩阵乘法
  - 基于矩阵乘法，我们可以对向量做很多变换，如下

$$\begin{pmatrix}
  -1 & 0\\
  0 & 1\\
\end{pmatrix}\begin{pmatrix}
  x\\
  y\\
\end{pmatrix}=
\begin{pmatrix}
  -x\\
  y\\
\end{pmatrix}$$

- 矩阵的转置
- 矩阵的逆
