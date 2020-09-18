# Transformation
今天将讲变换。其实变换也有很多分支，比如渲染出的图像的变换、骨骼的运动等等。

首先来看 2D 变换。
### 2D transformations
包括：
- 缩放 Scale Transform

$$\begin{bmatrix}
  x' \\
  y'
\end{bmatrix}=\begin{bmatrix}
 s_x & 0\\
 0 & x_y
\end{bmatrix}\begin{bmatrix}
 x \\
 y
\end{bmatrix}$$

- 映像 Reflection
- 错切 Shear
- 旋转 Rotation

上述变换都是基于原点的。这些都可以用2*2的矩阵做线性运算。

### 齐次坐标 Homogeneous Coordinates
然而，比如平移 Translation ，无法用2*2的矩阵做线性运算。

由此，考察矩阵的数学形式，提出了`齐次坐标`。描述空间中的点和向量时，多增加一个维度，这样便`可以把一切基础变换都归于矩阵乘法来进行`。

对于：
- 二维空间中的点 $(x, y, 1)^T$
- 二维空间中的向量 $(x, y, 0)^T$

或者说，对于点，只要 $(x, y, w)^T$ 中 $w$ 不等于 0 就行，其真实表示的 $(x,y)$ 总是等价于 $(x/w, y/w, 1)^T, w \neq 0$ 。

**值得注意的是：**
- 由于矩阵乘法不符合交换律，因此，如果想对 a 先进行 A 变换，再进行 B 变换，应该 $a'=BAa$
- 此外，矩阵的逆让变换还原 $a = A^{-1}B^{-1}a'$

### 3D Transforms
3D 齐次坐标同理。
