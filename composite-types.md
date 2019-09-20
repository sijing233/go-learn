---
description: Composite Types
---

# Composite Types

基础数据类型，经过复杂多样的变化，构建为复杂数据类型

* Arrays：数组
* Slices：切片
* maps：地图
* structs：结构体

### 4.1 结构体

定义：数组是一个有固定长度的序列

描述：通过下标描述数组，下标从0开始，最大为数组的长度-1

{% code-tabs %}
{% code-tabs-item title="test-4.go" %}
```go
var a [3]int  // a是一个数组，有三个整数，每一个元素初始为0
fmt.Println(a[0]) // 输出第一个元素
fmt.Println(a[len(a)-1]) //输出第二个元素

for i,v := range a {
    fmt.Println("%d %d\n",i,v) // i表示数组下标，v表示数组的内容
}

for _,v := range a {
	fmt.Printf("%d\n",v) // _可以省略返回下标
}

var q [3]int = [3]int{1,2,3}
var r [3]int = [3]int{1,2}
fmt.Println(r[2]) //0 r一共有2个元素，r[2]表示输出第三个元素，go里输出0，而不是出错
```
{% endcode-tabs-item %}
{% endcode-tabs %}





* 每一个数组，如果没有赋值，则初始化为0

{% code-tabs %}
{% code-tabs-item title="test.py" %}
```python
>>> a = [1,2]
>>> a[2]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
```
{% endcode-tabs-item %}
{% endcode-tabs %}

