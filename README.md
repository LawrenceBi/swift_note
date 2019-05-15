# swift_note

## 1. 结构体和类的区别
    1） 结构体类型实例化成员有逐一构造器，类没有
    2） 赋值或传递时，结构体是值传递，类是引用传递
    3） 结构体不可以继承，类可以
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
        
    3） Any和AnyObject
        Swift为不确定点类型，提供了两种特殊类型别名：AnyObject和Any。其中AnyObject可以代表任何class类型点实例，Any则可以表示任何类型，除了方法（function types）。
        
    4） typealias
        typealias是用来为已经存在的类型重新定义名字的,通过命名,可以使代码变得更加清晰。
        
    5） is 和 as
        is操作用来判断某一个对象是否是某一个特定的类，它会返回一个bool类型的值。is操作的逻辑很简单，某一个类的对象肯定是自己这个类，也一定是自己的父类，但父类的对象不是子类。如果两个类没有继承关系，那is操作一定返回false。
        
        as类型转换的规则是，子类可以向上转换为父类，但父类不能向下（downcast）转换为子类。除非某个子类的对象表现形式为父类，但实际是子类，这时可以使用as！进行向下转换（downcast）。
## 4. Thread, Operation 和 Grand Central Dispatch
    1)  Thread: 每个thread对象对应一个线程，优点是量级较轻，使用简单；缺点是需要开发者自行管理线程的生命周期、线程同步、加锁解锁、睡眠及唤醒等操作。
    2)  Operation: 不需要关心线程的管理和线程同步的事情，可以把精力放在自己需要执行的业务逻辑上，缺点是只能实现它定义好的子类。
    3)  Grand Central Dispatch: 是基于C语言的一种高效、强大的多核编辑解决方案，其在后端管理着一个线程池，它不仅仅决定代码块将在哪个线程被执行，还可以根据可用的系统资源对这些线程进行管理。

