# 说明：此文件会记录一些笔记    </br>

## Course 01 神经网络和深度学习    </br>

### Week 02 神经网络基础    </br>

### note1 向量化    </br>
* 别用 for、while等循环，还记得 向量化吗
* 预处理数据集的常见步骤是：    </br>
  1. 计算出问题的纬度、形状    </br>
  2. 将数据集中，每一个样本转化为向量。（lr中，将图片样例转化为一维向量）    </br>
  3. 标准化（可以减去每个示例中整个numpy数组的平均值， 然后将每个示例除以整个numpy数组的标准偏差。但对于图片数据集，它更简单，更方便，几乎可以将数据集的每一行除以255（像素通道的最大值）， 因为在RGB中不存在比255大的数据，所以我们可以放心的除以255，让标准化的数据位于[0,1]之间）    </br>

### note2 np.dot    </br>

* numpy.dot()          </br>
对于两个一维的数组，计算的是这两个数组对应下标元素的乘积和(数学上称之为内积)；    </br>
对于二维数组，计算的是两个数组的矩阵乘积；       </br>
对于多维数组，它的通用计算公式如下，      </br>
即结果数组中的每个元素都是：数组a的最后一维上的所有元素与数组b的倒数第二位上的所有元素的乘积和： dot(a, b)[i,j,k,m] = sum(a[i,j,:] * b[k,:,m])。    </br>
* ym注：         </br>
对于np.dot的多维运算可以参考二位运算的方法，就目前所遇见的例子，与线性代数中矩阵相乘的算法是一致的。    </br>
### note3 center and standardize dataset    </br> 
* One common preprocessing step in machine learning is to center and standardize your dataset, meaning that you substract the mean of the whole numpy array from each example, and then divide each example by the standard deviation of the whole numpy array. But for picture datasets, it is simpler and more convenient and works almost as well to just divide every row of the dataset by 255 (the maximum value of a pixel channel).
* 机器学习中一个常见的预处理步骤是对数据集进行居中和标准化，这意味着可以减去每个示例中整个numpy数组的平均值，然后将每个示例除以整个numpy数组的标准偏差。但对于图片数据集，它更简单，更方便，几乎可以将数据集的每一行除以255（像素通道的最大值），因为在RGB中不存在比255大的数据，所以我们可以放心的除以255，让标准化的数据位于[0,1]之间
* What you need to remember: --by wuenda     </br> 
Common steps for pre-processing a new dataset are:
1. Figure out the dimensions and shapes of the problem (m_train, m_test, num_px, ...)    </br> 
2. Reshape the datasets such that each example is now a vector of size (num_px * num_px * 3, 1)    </br> 
3. "Standardize" the data    </br> 

### note4 learning rate    </br>
* Choose the learning rate that better minimizes the cost function.    </br>
