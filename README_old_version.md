# SmartTable历史版本

###### 一款android自动生成表格框架

**- 1.4版本**

> 删除设置固定第一列setFixedFirstColumn方法，column的setFixed(boolean fixed)来固定任意列。
>支持首尾动态添加数据SmartTable.addData(List<T> t,boolean isFoot)来实现添加数据.实现增量解析数据和计算表格大小，效率更高。
> 修复缩放中心偏移问题；
> 支持内容多行显示。
![内容多行显示](/img/multline.jpg)
	

**- 1.3版本**

- 设置单个格子背景

>  在网上参考了```html```的```table```,发现样式好看多了，按到这个思路，SmartTable增加了支持对单个格子的不同背景支持，在```TableConfig```里面有5个```IBackgroundFormat```样式，可以根据```boolean isDraw(T t)```返回数据做出判断是否绘制背景```drawBackground```，默认绘制整个背景，当然你可以自己定义```IBackgroundFormat```使用其他形状。

- 设置单个格子字体

> 由于支持到单个格子背景的支持，字体颜色也需要根据背景还进行调整，所以又支持单个格子的字体设置，```IBackgroundFormat```中有 ```int getTextColor(T t)```,你只需重写它，根据需求设置不同颜色。

- 分页

> 在客户端太多数据体验不好，所以开发分页模式，在未使用注解情况下，只需要使用```PageTableData```分页表格数据类 代替之前```TableData```表格数据类即可，使用```PageTableData```的```setPageSize```方法设置每页数量。分页就完成了。
如果你使用注解，请在```@SmartTable```注解元素添加```pageSize```属性即可，setData会返回```PageTableData```对象，你可以使用它完成后面其他的设置。

- 其他

> SmartTable 增加notifyDataChanged方法用于重新解析计算布局；

> 提供back方法fling到原点；

> 增加网络请求图片显示例子。

**- 1.2版本**

> 自动统计，排序（也可自定义统计规则）；
>  表格批注；
> 缩放模式和滚动模式.

**- 1.1版本**

>  表格列标题组合；
>  表格固定左序列、顶部序列、第一行、列标题、统计行；
>  自动统计，排序（也可自定义统计规则）；

>  表格内容、列标题点击事件；



**- 1.0版本**

>  快速配置自动生成表格；
>  自动计算表格宽高；
>  表格各组成背景、文字、网格、padding等配置；
>  表格图文、序列号、列标题格式化；
>  支持注解模式。
