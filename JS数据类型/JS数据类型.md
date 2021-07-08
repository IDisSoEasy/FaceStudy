# JS数据类型
* 数据类型
  > 基础数据类型
    > > + 基础数据类型存储在栈内存，被引用或拷贝时会创建一个完全相等的变量
    > > + String、Boolean、Number、Null、Undefined、Symbol、Biglnt

  > 引用数据类型
    > > + 引用类型存储在堆内存，存储的是地址，多个引用指向同一个地址
    > > + Object、Array、Function、RegExp、Date、Math

* 判断数据类型
  > typeof
    > > + typeof 可以判断基础数据类型（null除外）
    > > + 但是引用数据类型中，处理function，其他的也无法判断

  > instanceof 
    > > + instanceof 可以准确地判断复杂数据类型
    > > + 但是不能判断基础数据了下

  > Object.prototype.toString.Call()
    > > + Object.prototype.toString.Call 可以准确的判断出引用数据和基础数据