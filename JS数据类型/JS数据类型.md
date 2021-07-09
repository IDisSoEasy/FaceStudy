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
    > > + 但是引用数据类型中，除了function，其他的也无法判断

  > instanceof 
    > > + instanceof 可以准确地判断复杂数据类型
    > > + 但是不能判断基础数据了下

  > Object.prototype.toString.Call()
    > > + Object.prototype.toString.Call 可以准确的判断出引用数据和基础数据
  
* 数据类型转换
  > - 强制类型转换
  > > + Number()  
  > > > - 如果是布尔值，true 和 false 分别被转换为 1 和 0  
  > > > - 如果是数字，返回自身  
  > > > - 如果是 null，返回 0  
  > > > - 如果是 undefined，返回 NaN  
  > > > - 如果是字符串，遵循以下规则：如果字符串中只包含数字（或者是 0X / 0x 开头的十六进制数字字符串，允许包含正负号），则将其转换为十进制；如果字符串中包含有效的浮点格式，将其转换为浮点数值；如果是空字符串，将其转换为 0；如果不是以上格式的字符串，均返回 NaN  
  > > > - 如果是 Symbol，抛出错误  
  > > > - 如果是对象，并且部署了 [Symbol.toPrimitive] ，那么调用此方法，否则调用对象的 valueOf() 方法，然后依据前面的规则转换返回的值；如果转换的结果是 NaN ，则调用对象的 toString() 方法，再次依照前面的顺序转换返回对应的值  
  > > + String()  
  > > + Boolean()  
  > > > - 除了 undefined、 null、 false、 ''、 0（包括 +0，-0）、 NaN 转换出来是 false，其他都是 true  
  > > + parseInt()  
  > > + toString()  
  > - 隐式类型转换