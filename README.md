# 如何实现数组去重？

**假如有数组arr=[1,5,2,3,4,2,3,1,3,4],写一个函数unique，使得unique(arr)的值为[1,5,2,3,4],把多余的值去掉。**

1. 使用ES6的set去重
```javascript
function unique(arr){
    return Array.from(new Set(arr));
}
```
该方法代码量最少，但在兼容性上有所不足，而且该方法无法去除空对象。

2.利用Map数据结构去重
```javascript
function unique(arr){
    let map =new Map();
    let array=new Array;
    for(let i=0;i<arr.length;i++){
        if(map.has[arr[i]]){
            map.set(arr[i]);
        }else{
            map.set(arr[i],false);
            array.push(arr[i]);
        }
    }
    return array;
}
```
该方法可以去除空对象，而且兼容性较强，但使用该方法效率较set略低且代码量多。
