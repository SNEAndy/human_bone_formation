# human_bone_formation
近年来随着三维数字人生成方法的发展，以及业界丰富的数字人需求，三维人体动画成为了图形学的一个重要方向。
而驱动一个三维人体网格，最常见的算法是骨架动画，它需要将三维网格绑定一套骨骼与蒙皮权重才能进行驱动。这个往往需要花费模型师数小时时间才能完成。
该赛题旨在使用各类3D深度神经网络结构，用于理解三维人体网络架构并预测相对应的骨骼节点的空间位置、以及对应的蒙皮权重。

本赛题将提供一批3D人体网格模型以及对应的骨骼位置、蒙皮权重，并要求参赛者依据3D人体骨骼格式介绍，对这些模型预测骨骼节点的空间位置以及蒙皮权重。即输入一个三维网格 M，需要预测出 J 个三维坐标表示骨骼节点的位置，以及 N×J 的矩阵表示原网格中 N 个点对于 J 个骨骼的蒙皮权重取值。
# 评测指标
比赛分为A、B两个榜单。A榜结束后将按排名筛选、审核让若干支队伍进入B榜。

赛题评测指标为三个指标， 含义如下：

CD-J2J：Chamfer Distance from Joints to Joints

衡量预测骨骼节点与真实骨骼节点之间的空间距离
使用Chamfer距离度量，反映骨骼位置预测的准确性
Skin-L1：L1 Loss from Skin to Skin

使用L1损失函数衡量预测的蒙皮权重与真实蒙皮权重之间的差异
反映权重预测的精确度
Vertex：Vertex Distance Loss

评估在应用骨骼和权重后，变形网格顶点与目标顶点之间的误差
反映最终骨骼动画效果的视觉质量