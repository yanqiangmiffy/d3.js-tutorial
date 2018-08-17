# d3.js-tutorial
d3.js 学习资料与教程

## D3.js 入门教程
- 地址：http://wiki.jikexueyuan.com/project/d3wiki/
- 目录：
  - 01-hello_world.html
  - 02-select-bind.html

    **选择元素**：
    ```
    d3.select()：是选择所有指定元素的第一个
    d3.selectAll()：是选择指定元素的全部
    ```
    **绑定数据**：
    ```
    datum()：绑定一个数据到选择集上
    data()：绑定一个数组到选择集上，数组的各项值分别与选择集的各元素绑定
    ```
    **改变元素的其他方法**
    ```
    selection.attr(name[, value]) 改变元素的属性值

    eg:a.attr("href","https://www.baidu.com")

    selection.text([value])  改变元素的文本

    selection.style(name[, value[, priority]]) 改变元素的样式

    selection.classed(names[, value]) 给元素添加css样式
    ```
  - 03-select-insert-delete.html

    **插入元素**：
    ```
    append()：在选择集末尾插入元素
    insert()：在选择集前面插入元素
    ```
    **插入元素**：
    ```
    删除一个元素时，对于选择的元素，使用 remove
    ```
  - 04-svg.html
  ```
  SVG，指可缩放矢量图形（Scalable Vector Graphics），是用于描述二维矢量图形的一种图形格式，是由万维网联盟制定的开放标准。

  SVG 使用 XML 格式来定义图形，除了 IE8 之前的版本外，绝大部分浏览器都支持 SVG，可将 SVG 文本直接嵌入 HTML 中显示。
  ```
  ![](https://github.com/yanqiangmiffy/d3.js-tutorial/blob/master/assets/04-svg.png)

  - 05-scale-linear.html
  ```
  比列尺：将某一区域的值映射到另一区域，其大小关系不变。

  线性比例尺，能将一个连续的区间，映射到另一区间。要解决柱形图宽度的问题，就需要线性比例尺。

  ```
  ```
  假设有以下数组：

    var dataset = [1.2, 2.3, 0.9, 1.5, 3.3];
    现有要求如下：

    将 dataset 中最小的值，映射成 0；将最大的值，映射成 300。

    代码如下：

    var min = d3.min(dataset);
    var max = d3.max(dataset);

    var linear = d3.scale.linear()
            .domain([min, max])
            .range([0, 300]);

    linear(0.9);    //返回 0
    linear(2.3);    //返回 175
    linear(3.3);    //返回 300
  ```
  ![](https://github.com/yanqiangmiffy/d3.js-tutorial/blob/master/assets/04-svg.png)