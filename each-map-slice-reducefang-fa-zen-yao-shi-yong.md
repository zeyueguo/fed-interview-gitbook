# each, map, slice, reduce方法怎么使用

## 数组的方法

### 1. forEach

让数组每一项做一件事

### 2. map

让数组通过某种计算产生新数组

### 3. filter

筛选出数组中符合条件的项，组成新数组

### 4. reduce

让数组中的前一项和后一项做某种计算，并累计最终值

### 5. every

检测数组中的每一项是否都符合条件，返回布尔值（全部符合才为true）

### 6. some

检测数组中是否至少一项符合条件，返回布尔值5

### 7. concat

合并数组，并返回新数组（不会改变原数组）

### 8. push

在原数组上操作（改变的是原数组）

### 9. slice

接受一个或两个参数，即要返回项的起始和结束位置。当只给slice\(\)传递一个参数时，该方法返回从该参数指定位置开始到当前数组末尾的所有项（不会改变原数组）

### 10. splice

方法中指定两个参数，第一个参数是指定开始删除数组项位置，第二个数是指删除数组项的个数

* 删除： 可以删除任意数量的数组项

* 插入： 可以向指定位置插入任意数量的数组项 

第三个参数是要插入的数组项。如果要插入多个项，可以再传入第四、第五、以至任意多个项

       `var arr2 = arr.splice(2,0,'a','b','c','d');`

* 替换： 可以向指定位置插入任意数量的数组项，且同时删除任意数量的数组项



## 

## 参考

[JavaScript学习笔记：数组的concat\(\)、slice\(\)和splice\(\)方法著作权归作者所有。](https://www.w3cplus.com/javascript/array-part-5.html)

[如何形象地解释 JavaScript 中 map、foreach、reduce 间的区别？ - 水乙的回答 - 知乎 ](https://www.zhihu.com/question/24927450/answer/77479376)

