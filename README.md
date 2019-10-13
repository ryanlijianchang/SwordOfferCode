### 1.二维数组中的查找 ###

**题目描述**

在一个二维数组中（每个一维数组的长度相同），每一行都按照从左到右递增的顺序排序，每一列都按照从上到下递增的顺序排序。请完成一个函数，输入这样的一个二维数组和一个整数，判断数组中是否含有该整数。

**题解思路**

- (1)暴力法
    - 解释：遍历每一个数组，直到遍历所有元素
    - 时间复杂度：O(n^2^)
    - 空间复杂度：O(1)
- (2)按列二分查找
    - 解释：从左到右（或从右到左），每一列进行二分查找，直到找到元素。
    - 时间复杂度：O(nlogn)
    - 空间复杂度：O(1)
- (3)从左下开始查找
    - 解释：先从左下角元素开始，如果该元素大于target，则往上找，如果该元素小于target，则往右找
    - 时间复杂度：O(w+h)
    - 空间复杂度：O(1)

**题解代码**

[Topic1.java](https://github.com/ryanlijianchang/SwordOfferCode/blob/master/Topic1.java)

### 2.替换空格 ###

**题目描述**

请实现一个函数，将一个字符串中的每个空格替换成“%20”。例如，当字符串为We Are Happy.则经过替换之后的字符串为We%20Are%20Happy。

**题解思路**
- (1)暴力法
    - 解释：先从前往后遍历字符串数组，确定空格个数，然后用一个新的数组，大小是旧数组大小+空格个数*2，然后从前往后遍历旧数组，遇到空格则追加"%20"，非空格则追加字符，最后输出。
    - 时间复杂度：O(n)
    - 空间复杂度：O(n)
    
**题解代码**
[Topic2.java](https://github.com/ryanlijianchang/SwordOfferCode/blob/master/Topic2.java)


### 3.从尾到头打印链表 ###

**题目描述**

输入一个链表，按链表从尾到头的顺序返回一个ArrayList。

**题解思路**

- (1)栈
    - 解释：要实现倒序输出，其实就是利用了栈的先进后出的思想。
    - 时间复杂度：O(n)
    - 空间复杂度：O(n)
- (2)递归
    - 解释：任何用栈实现的算法，都是可以用递归来实现，可以理解成每一次插入元素都是在后一个元素已经插入的基础上进行。
    - 时间复杂度：O(n)
    - 空间复杂度：O(n)

**题解代码**

[Topic3.java](https://github.com/ryanlijianchang/SwordOfferCode/blob/master/Topic3.java)

### 4.重建二叉树 ###

**题目描述**

输入某二叉树的前序遍历和中序遍历的结果，请重建出该二叉树。假设输入的前序遍历和中序遍历的结果中都不含重复的数字。例如输入前序遍历序列{1,2,4,7,3,5,6,8}和中序遍历序列{4,7,2,1,5,3,8,6}，则重建二叉树并返回。

**题解思路**

- (1)递归
    - 解释：前序遍历获取到的第一个元素就是根结点，找到根结点在中序遍历中的位置i，则位置i左边的元素都是根结点的左子树，位置i右边的元素都是根结点的右子树，所以前序遍历的第1个元素就是左子树结点，前序遍历的第i+1个元素就是右子树结点，然后如此递归遍历即可。
    - 时间复杂度：O(n)。只需要遍历n个结点即可完成。
    - 空间复杂度：O(n)。额外申请了n个元素的空间。
    

**题解代码**

[Topic4.java](https://github.com/ryanlijianchang/SwordOfferCode/blob/master/Topic4.java)
