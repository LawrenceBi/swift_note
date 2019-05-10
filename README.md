# swift_note

## 1. 结构体和类的区别
    1） 结构体类型实例化成员有逐一构造器，类没有
    2） 赋值或传递时，结构体是值传递，类是引用传递
## 2. 安全拆包的方法
    Swift推荐的方式是在if语句中使用let关键字创建一个新的变量，并且让这个变量等于可选变量的值，如果可选变量有真正的值，则会执行if语句的相关代码，这就 是可选绑定。
    
    var destination: String?
    ...
    if let userDestination = destination {
        print("目的地: " + userDestination)
    }
    
