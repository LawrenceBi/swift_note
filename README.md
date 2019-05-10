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
## 3. 一些关键字
    1） subscript: 下标脚本
        下标脚本 可以定义在类（Class）、结构体（structure）和枚举（enumeration）这些目标中，可以认为是访问对象、集合或序列的快捷方式，不需要再调用实例的特定的赋值和访问方法。
        举例来说，用下标脚本访问一个数组(Array)实例中的元素可以这样写 someArray[index] ，访问字典(Dictionary)实例中的元素可以这样写 someDictionary[key]。
        
    2） assert: 断言
        在 Swift 语言中可以调用全局的 assert 函数来增加一个断言，这里的全局意思是你可以将断言放在你程序的任何一个地方，程序在执行到 assert 时会判断其中的逻辑条件表达式参数是否为 true。
        a.如果条件判断为 true，代码运行会继续进行。
        b.如果条件判断为 false，程序将终止。
