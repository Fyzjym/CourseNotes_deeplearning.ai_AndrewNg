# 说明：此文件会记录一些问题

## Course 01 神经网络和深度学习
### Week 02 神经网络基础

* Q1:吴大佬引入神经网络的例子为logistic regression模型。对于LR模型中，为啥要把参数w、b初始化为np.zeros(shape = (dim,1))、0呢？  <br>
* A1：资源  <br>
      * https://blog.csdn.net/qq_36814762/article/details/102469333  <br>
      * https://zhuanlan.zhihu.com/p/75879624  <br>
      * https://www.jianshu.com/p/02b529634868  <br>

* Q2：当对（sample_number，img_px, img_px, channel_num）矩阵转化为（img_px * img_px * channel_num, sample_number）矩阵。  <br>
      *   X.reshape(X.shape[0], -1).T可以将一个维度为(a,b,c,d)的矩阵转换为一个维度为(b∗c∗d, a)的矩阵。  <br>
      * code：  X_flatten = X.reshape(X.shape [0]，-1).T ＃X.T是X的转置  <br>
* A2：理解     <br>
      * https://blog.csdn.net/TeFuirnever/article/details/88919206  <br>
