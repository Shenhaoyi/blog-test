# 介绍一下我的个人情况

我最近在做的事情：
1. 学习前端准备找工作
2. 准备开题材料
3. 准备下一次组会内容

我喜欢的歌手或乐队有：
* 林俊杰
* 苏打绿
* 王力宏
* 许嵩
* ……

`HTML` `CSS`和`JS`我都学了一点，但是都比较基础，最近也有用`JS`在leetcode刷题，写一个二叉树的前序遍历展示下吧
```js
var preorderTraversal = function(root) {
    //空检测
    if(!root) return [];
    let result = [];

    //非递归
    //使用栈，弹出自己，压入右，再压入左，
    let stack = [root],
        current = null;
    while (stack.length !== 0){
        current = stack.pop();
        result.push(current.val);
        current.right && stack.push(current.right);
        current.left && stack.push(current.left);
    }

    return result;
};
```

