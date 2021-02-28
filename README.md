# bulinx-C5-imu_cali

ubuntu 18.04 melodic 参考[here](src/imu_tk/README.md), 自行完成环境配置


---

## 推导加速度计对应残差对加速度内参的雅可比
公式推导按照a=(I-Sa)Ka(A-ba),代码中按照公式min_mat展开，符号相对应，结构大同小异。

---
<img src="doc/images/q1.jpg" alt="Mapping and Map-Based Localization" width="100%">



## 改加速度计内参模型为下三角，构建ceres解析式求导，仿真数据做验证

创造CaliAccCostFunction类，继承自SizedCostFunction
下三角模型修改处：
[chang1]
[chang2]
[chang3]
雅克比构建：
[chang4]
ceres解析式修改：
[chang5]
标定结果如下：
<img src="doc/images/zhongduan1.png" alt="IMU TK, Shell Output" width="100%">

<img src="doc/images/2.png" alt="IMU TK, GNU Plot Visualization" width="100%">




