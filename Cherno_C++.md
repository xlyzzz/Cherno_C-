---
html:
    toc: true
    # number_sections: true
    toc_depth: 6
    toc_float: true
        collapsed: true
        smooth_scroll: true
--- 
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [一. 欢迎来到C++][1]
  - [1.1 使用C++的最大直接原因是直接控制硬件]()
  - [1.2 本地计算机语言]()
- [二. Windows上安装C++]()
  - [2.1 Microsoft Visual Studio][2]
  - [2.2 Visual Assist][3]
  - [2.3 TOOLS->Import and export Settings]()
  - [2.4 项目路径最好别有空格和中文]()
- [三. Mac上安装C++]()
- [四. Linux上安装C++]()
- [五. C++是如何工作的]()
  - [5.1 Project Property]()
  - [5.2 编译单个cpp文件，Ctrl+F7]()
  - [5.3 vs右键单击工具栏->Customize->Commands->Add Commands->Build->Compile 添加Compile工具栏按钮]()
  - [5.4 只有cpp文件会被编译成object file]()
  - [5.5 看输出窗口尽量看Output，别看Error List]()
  - [5.6 Linker将多个obj文件链接起来]()
- [六. C++编译器是如何工作的]() 
  - [6.1 Property->C/C++->Preprocessor->Preprocess to a File]()
  - [6.2 Property->C/C++->Output Files->Assembler Output->Assembly-Only Listing (/FA)]()
  - [6.3 Property->C/C++->Optimization->Optimization]()
- [七. C++链接器是如何工作的]()
  - [7.1 学会区分编译阶段和链接阶段的错误，编译错误一般以C开头，链接错误以LNK开头]()
  - [7.2 Property->Linker->Advanced->Entry Point]()
  - [7.3 函数前面加上static，意味着函数只被声明在该翻译单元]()
  - [7.4 函数前面加上inline，将函数调用替换为函数体]()
- [八. C++变量]()
  - [8.1 float数定义时加上‘f’后缀]()
  - [8.2 sizeof()操作符获取类型内存大小]()
- [九. C++函数]()
  - [9.1 做一项共同的任务多次，封装成函数]()
  - [9.2 函数的主要目的是防止代码重复]()
  - [9.3 注意程序在Debug和Release模式下的不同]()
- [十. C++头文件]()
  - [10.1 #pragma once、#ifndef防止头文件重复包含]()
  - [10.2 <>通常用来包含系统头文件，“”用来包含项目相对路径下的头文件]()
  - [10.3 系统文件间右键单击->Open Document, 系统头文件右键单击->Open Containing Folder查看系统文件代码]()
- [十一. 如何在Visual Studio中调试代码]()
  - [11.1 Step Into(F11), Step Out(Ctrl+F11), Step Over(F10)]()
  - [11.2 F5运行程序直到碰到下一个断点]()
  - [11.3 调试时黄色箭头表示下一步将要执行的代码，但还未执行]()
  - [11.4 Autos、Locals窗口查看局部变量值，Watch1监视想要查看的变量值]()
  - [11.5 Debug->Windows->Memory->Memory1查看内存视图]()
- [十二. C++条件与分支]()
  - [12.1 分支会减慢程序的运行]()
  - [12.2 调试时鼠标单机右键->Go To Disassembly查看汇编代码]()
  - [12.3 False实际上是0，True实际上是除0外的任何数]()
  - [12.4 else if其实不是C++的关键字，只是把else和if放到了同一行而已]()
  - [12.5 编程可分成数学编程和逻辑编程，在合适的时候用数学编程代替逻辑编程可以提高程序运行速度]()
- [十三. Visual Studio的最佳设置]()
  - [13.1 Solution Explorer->Show All Files显示磁盘实际的目录结构]()
  - [13.2 Properties->General->Output Directory "$(SolutionDir)bin\$(Platform)\$(Configuration)\"]()
  - [13.2 Properties->General->Intermediate Directory "$(SolutionDir)bin\intermediates\$(Platform)\$(Configuration)\"]()
- [十四. C++循环]()
  - [14.1 for, while, do while]()
- [十五. C++控制流语句(continue, break, return)]()
- [十六. C++指针]()
  - [16.1 指针实质是一个保存了内存地址的整数]()
- [十七. C++引用]()
- [十八. C++类]()
  - [18.1 数据和处理这些数据的函数构成]()
- [十九. C++类与结构体对比]()
  - [19.1 类默认可见度为pirvate，结构体默认可见度为public]()
  - [19.2 类的继承]()
- [二十. 如何写一个C++类]()
- [二十一. C++中的静态(static)]()
  - [21.1 类(或结构体)外面的static，意味着它只对定义它的翻译单元可见，翻译单元内部链接]()
  - [21.2 类(或结构体)内的static，意味着静态变量或者函数被类的所有实例共享内存]()
  - [21.3 extern关键字意味着会在外部翻译单元中寻找某个变量]()
  - [21.4 少用全局变量]()
- [二十二. C++类和结构体中的静态(static)]()
  - [22.1 类的static变量需在类外初始化(静态成员变量是所有实例共享的，但是其只是在类中进行了声明，并未定义或初始化（分配内存），类或者类实例就无法访问静态成员变量，这显然是不对的，所以必须先在类外部定义，也就是分配内存)]()
  - [22.2 静态方法不能访问非静态变量]()
- [二十三. C++中的局部静态(static)]()
  - [23.1 变量的生存期和作用域]()
- [二十四. C++枚举]()
  - [24.1 枚举的本质就是整数的集合]()
  - [24.2 枚举变量的命名一般用枚举名+信息(例如：LevelError)]()
- [二十五. C++构造函数]()
  - [25.1 对象初始化时自动调用的函数]()
- [二十六. C++析构函数]()
  - [26.1 对象销毁时自动调用的函数]()
- [二十七. C++继承]()
  - [27.1 继承的作用之一是去掉重复的代码]()
  - [27.2 子类继承了父类所有的东西]()
  - [27.3 多态是一个单一类型，但有“多个类型”的意思]()
- [二十八. C++虚函数]()
  - [28.1 虚函数表包含基类中所有虚函数的映射]()
  - [28.1 虚表会产生额外的开销，包括基类中要有一个成员指针指向虚表，其次，当调用虚函数时需要遍历虚表，来确定要映射到哪个虚函数]()
- [二十九. C++接口(纯虚函数)]()
- [三十. C++可见性]()
  - [30.1 private、protected、public]()
- [三十一. C++数组]()
  - [31.1 直接寻址和间接寻址，应该尽量在栈上创建数组来避免间接寻址]()
  - [31.2 原始数组需要自己手动维护size]()
  - [31.3 std::array]()
- [三十二. C++字符串]()
  - [32.1 ascii表][4]
  - [32.2 c字符串以‘\0’结尾]()
  - [32.3 std::string]()
- [三十三. C++字符串字面量]()
  - [33.1 字符串字面量永远保存在内存的只读区域内]()
  - [33.2 字符串字面量定义时前面加const]()
  - [33.3 字符串字面量前加‘R’忽略转义字符]()
- [三十四. C++中的const]()
  - [34.1 成员函数加const表示不会修改成员变量的值]()
  - [34.2 常量引用]()
  - [34.3 mutable]()
- [三十五. C++中的mutable]()
  - [35.1 const成员函数修改成员变量时用到(mutable最常用到的地方)]()
  - [35.2 lambda表达式中用到(基本不用用到)]()


[1]: https://www.bilibili.com/video/BV1uy4y167h2/
[2]: https://visualstudio.microsoft.com/
[3]: https://www.wholetomato.com/
[4]: https://www.asciitable.com/

<!-- /code_chunk_output -->






