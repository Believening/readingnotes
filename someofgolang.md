###  golang 特性相关

* golang `var name = XXXXX()` 和 `:=` 形式的类型推断带来的好处？  
   类型推断是在编译时完成的，并不会影响程序执行时的效率，但是在编写过程中一定程度上能够体会到动态类型语言的便利。与此同时，类型推断会使得代码重构更加方便，增加了程序的灵活性；因为其静态类型语言，一旦变量初始化是确定类型，后续都不可以改变，维护性更高。

* goalang 的重声明发生的条件  
  * 在同一个代码块中
  * 使用 `:=` 来完成
  * 必须是在申明多个变量中新旧变量混在一起的情况
  * 与原变量类型要保持一致

### golang 语法相关 

* 模块级别私有  
  internal 代码包的使用
  ```
  src
    project_name
        ├─packageA_name
        │     ├─internal
        │     │     └─internal.go // 此源码文件内的文件非私有程序实体，包外无法访问
        │     └─xxx.go
        └─packageB_name  
  ```