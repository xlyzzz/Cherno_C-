---
html:
    toc: true
    # number_sections: true
    toc_depth: 6
    toc_float: true
        collapsed: true
        smooth_scroll: true
--- 
<!-- @import "TOC" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->
- [一. 欢迎来到C++][1]
  - 1.1 使用C++的最大直接原因是直接控制硬件
  - 1.2 本地计算机语言
- 二. Windows上安装C++
  - [2.1 Microsoft Visual Studio][2]
  - [2.2 Visual Assist][3]
  - 2.3 TOOLS->Import and Export Settings
  - 2.4 项目路径最好别有空格和中文
- 三. Mac上安装C++
- 四. Linux上安装C++
- 五. C++是如何工作的
  - 5.1 Project Property
  - 5.2 编译单个cpp文件，Ctrl+F7
  - 5.3 vs右键单击工具栏->Customize->Commands->Add Commands->Build->Compile 添加Compile工具栏按钮
  - 5.4 只有cpp文件会被编译成object file
  - 5.5 看输出窗口尽量看Output，别看Error List
  - 5.6 Linker将多个obj文件链接起来
- 六. C++编译器是如何工作的
  - 6.1 Property->C/C++->Preprocessor->Preprocess to a File 生成预处理后的文件(不会生成.obj文件)
  - 6.2 Property->C/C++->Output Files->Assembler Output->Assembly-Only Listing (/FA) 生成汇编文件
  - 6.3 Property->C/C++->Optimization->Optimization 查看优化等级
- 七. C++链接器是如何工作的
  - 7.1 学会区分编译阶段和链接阶段的错误，编译错误一般以C开头，链接错误以LNK开头
  - 7.2 Property->Linker->Advanced->Entry Point 定义入口函数名称
  - 7.3 函数前面加上static，意味着函数只被声明在该翻译单元
  - 7.4 函数前面加上inline，将函数调用替换为函数体
- 八. C++变量
  - 8.1 float数定义时加上‘f’后缀
  - 8.2 sizeof操作符获取类型内存大小
- 九. C++函数
  - 9.1 做一项共同的任务多次，封装成函数
  - 9.2 函数的主要目的是防止代码重复
  - 9.3 注意程序在Debug和Release模式下的不同
- 十. C++头文件
  - 10.1 #pragma once、#ifndef防止头文件重复包含
  - 10.2 <>通常用来包含系统头文件，“”用来包含项目相对路径下的头文件
  - 10.3 右键单击#include包含的头文件->Open Document查看系统头文件源码, 系统头文件右键单击->Open Containing Folder查看系统文件位置
- 十一. 如何在Visual Studio中调试代码
  - 11.1 Step Into(F11), Step Out(Ctrl+F11), Step Over(F10)，Continue(F5)
  - 11.2 F5运行程序直到碰到下一个断点
  - 11.3 调试时黄色箭头表示下一步将要执行的代码，但还未执行
  - 11.4 Autos、Locals窗口查看局部变量值，Watch1监视想要查看的变量值
  - 11.5 Debug->Windows->Memory->Memory1查看内存视图
- 十二. C++条件与分支
  - 12.1 分支会减慢程序的运行
  - 12.2 调试时鼠标单机右键->Go To Disassembly查看汇编代码
  - 12.3 False实际上是0，True实际上是除0外的任何数
  - 12.4 else if其实不是C++的关键字，只是把else和if放到了同一行而已
  - 12.5 编程可分成数学编程和逻辑编程，在合适的时候用数学编程代替逻辑编程可以提高程序运行速度
- 十三. Visual Studio的最佳设置
  - 13.1 Solution Explorer->Show All Files显示磁盘实际的目录结构
  - 13.2 Properties->General->Output Directory "$(SolutionDir)bin\$(Platform)\$(Configuration)\"
  - 13.2 Properties->General->Intermediate Directory "$(SolutionDir)bin\intermediates\$(Platform)\$(Configuration)\"
- 十四. C++循环
  - 14.1 for, while, do while
- 十五. C++控制流语句(continue, break, return)
- 十六. C++指针
  - 16.1 指针实质是一个保存了内存地址的整数
- 十七. C++引用
- 十八. C++类
  - 18.1 数据和处理这些数据的函数构成
- 十九. C++类与结构体对比
  - 19.1 类默认可见度为pirvate，结构体默认可见度为public
  - 19.2 类的继承
- 二十. 如何写一个C++类
- 二十一. C++中的静态(static)
  - 21.1 类(或结构体)外的static，意味着它只对定义它的翻译单元可见，翻译单元内部链接
  - 21.2 类(或结构体)内的static，意味着静态变量或者函数被类的所有实例共享内存
  - 21.3 extern关键字意味着会在外部翻译单元中寻找某个变量
  - 21.4 少用全局变量
- 二十二. C++类和结构体中的静态(static)
  - 22.1 类的static变量需在类外初始化(静态成员变量是所有实例共享的，但是其只是在类中进行了声明，并未定义或初始化（分配内存），类或者类实例就无法访问静态成员变量，这显然是不对的，所以必须先在类外部定义，也就是分配内存)
  - 22.2 静态方法不能访问非静态变量
- 二十三. C++中的局部静态(static)
  - 23.1 变量的生存期和作用域
- 二十四. C++枚举
  - 24.1 枚举的本质就是整数的集合
  - 24.2 枚举变量的命名一般用枚举名+信息(例如：LevelError)
- 二十五. C++构造函数
  - 25.1 对象初始化时自动调用的函数
- 二十六. C++析构函数
  - 26.1 对象销毁时自动调用的函数
- 二十七. C++继承
  - 27.1 继承的作用之一是去掉重复的代码
  - 27.2 子类继承了父类所有的东西
  - 27.3 多态是一个单一类型，但有“多个类型”的意思
- 二十八. C++虚函数
  - 28.1 虚函数表包含基类中所有虚函数的映射
  - 28.1 虚表会产生额外的开销，包括基类中要有一个成员指针指向虚表，其次，当调用虚函数时需要遍历虚表，来确定要映射到哪个虚函数
- 二十九. C++接口(纯虚函数)
- 三十. C++可见性
  - 30.1 private、protected、public
- 三十一. C++数组
  - 31.1 直接寻址和间接寻址，应该尽量在栈上创建数组来避免间接寻址
  - 31.2 原始数组需要自己手动维护size
  - 31.3 std::array
- 三十二. C++字符串
  - [32.1 ascii表][4]
  - 32.2 c字符串以‘\0’结尾
  - 32.3 std::string
- 三十三. C++字符串字面量
  - 33.1 字符串字面量永远保存在内存的只读区域内
  - 33.2 字符串字面量定义时前面加const
  - 33.3 字符串字面量前加‘R’忽略转义字符
  - 33.4 多行字符串定义（每行字符串用“”包含起来）
  - 33.5 宏的定义只能在一行，宏定义多行时，在除最后一行的每行后面加\
- 三十四. C++中的const
  - 34.1 成员函数加const表示不会修改成员变量的值
  - 34.2 常量引用
  - 34.3 mutable
- 三十五. C++中的mutable
  - 35.1 const成员函数修改成员变量时用到(mutable最常用到的地方)
  - 35.2 lambda表达式中用到(基本不会用到)
- 三十六. C++的成员初始化列表
  - 36.1 成员变量按照定义的顺序进行初始化
  - 36.2 成员变量为类对象时，赋值初始化会调用两次构造函数浪费性能，这时用成员初始化列表
- 三十七. C++的三元操作符
  - 37.1 三元操作符用来对if else进行精简，可嵌套使用
- 三十八. 创建并初始化C++对象
  - 38.1 尽量在栈上创建对象，速度快
- 三十九. C++ new关键字
  - 39.1 new会调用构造函数，malloc不会
- 四十. C++隐式转换与explicit关键字
  - 40.1 C++允许编译器对代码执行一次隐式转换
- 四十一. C++运算符及其重载
- 四十二. C++的this关键字
  - 42.1 this是一个指向当前对象实例的指针
- 四十三. C++的对象生存期(栈作用域生存期)
- 四十四. C++的智能指针
  - 44.1 unique_ptr 作用域指针
  - 44.2 shared_ptr 使用了引用计数
  - 44.3 weak_ptr 将share_ptr赋值给weak_ptr时，不会增加引用计数
- 四十五. C++的赋值与拷贝构造函数
  - 45.1 浅拷贝和深拷贝（浅拷贝只拷贝指针的值，深拷贝拷贝指针所指向的内存值）
  - 45.2 总是通过const引用传递对象
  - 45.3 String second = string调用的是拷贝构造函数
  - 45.4 String second; second = string调用的是拷贝赋值函数
- 四十六. C++的箭头操作符
- 四十七. C++的动态数组(std::vector)
  - 47.1 vector中尽量使用对象(而不是指针)
- 四十八. C++的std::vector使用优化
  - 48.1 vector中频繁地触发allocate是拖慢程序的原因之一
  - 48.2 vector reserve
  - 48.3 vector emplace_back
- 四十九. C++中使用库(静态链接)
  - 49.1 下载库是32位还是64位取决于自己的应用程序的位数
  - 49.2 static library库会被放到你的可执行文件中
  - 49.3 dynamic library是在运行时被链接的
  - 49.4 LoadLibrary
  - 49.5 使用库步骤：a.Property->C/C++->General->Additional Include Directories b.Property->Linker->General->Additional Library Dependencies c.Property->Linker->Input->Additional Dependencies
  - 49.6 还可以把库源码放到工程中自己构建
  - 49.7 函数声明前加extern "C”，作用是对在C++中使用C语言编译的库时，让C函数保持原貌
  - 49.8 运行时链接中如何提取函数(Loadlibrary和GetProcAddress)
- 五十. C++中使用动态库
  - 50.1 静态链接允许更多的优化发生
  - 50.2 使用动态库时记得把动态库(dll)拷贝到exe文件目录下
  - 50.3 _declspec(dllimport)
- 五十一. C++中创建与使用库
  - 51.1 项目右键->Add->Reference为项目添加同一个解决方案下的依赖库
  - 51.2 生成动态库时，在声明和定义的函数前均加上_declspec(dllexport),即可同时生成dll与lib
  - 51.3 生成动态库时，在动态库项目Property->Build Events->Post-Build Event->Command Line设置生成后事件，自动将dll文件拷贝到可执行目录文件夹
- 五十二. C++中如何处理多返回值
  - 52.1 使用引用和指针作为函数参数，指针作函数参数时可以是无效的(nullptr)
  - 52.2 std::vector(堆), std::arrary(栈)
  - 52.3 std::tuple, std::pair
  - 52.4 结构体作为函数的返回对象(应该是最好的方式)
- 五十三. C++的模板
  - 53.1 所谓模板，就是基于一定的规则，让编译器为你写代码
  - 53.2 模板在其被调用时才真正创建，编译期创建
  - 53.3 适当使用模板
- 五十四. C++的堆与栈内存的比较
  - 54.1 栈上分配就一条CPU指令
  - 54.2 栈的分配非常快，多个变量的内存地址很近
  - 54.3 堆的分配变量内存地址是离散的，同时还要记录很多东西
  - 54.4 new底层实际调用malloc函数，程序会维护空闲列表(free list)
  - 54.5 Cache Hit、Cache Miss
  - 54.6 堆和栈的性能差异来源于分配
- 五十五. C++的宏
  - 55.1 Property->C/C++->Preprocessor->Preprocessor Definitions
  - 55.2 宏必须在同一行，可用\代替换行
  - 55.3 宏对于调试非常有用
- 五十六. C++的auto关键字
  - 56.1 一般在使用长类型名时用auto代替
  - 56.2 using、typedef
- 五十七. C++的静态数组(std::array)
  - 57.1 array和c数组性能一样，自身维护了size大小，并且可使用标准算法函数
- 五十八. C++的函数指针
  - 58.1 auto关键字对于函数指针之类的东西非常有用
  - 58.2 函数指针作函数参数
  - 58.3 lambda(匿名函数)
  - 58.4 回调函数
- 五十九. C++的lambda
  - 59.1 lambda像是一个快速的一次性函数
  - 59.2 std::function与c函数指针
- 六十. 为什么不使用using namespace std
  - 60.1 使用命名空间前缀可以显示所属的库
  - 60.2 当多个命名空间有同名函数时，容易引入混乱
- 六十一. C++的命名空间
  - 61.1 命名空间的主要目的是避免命名冲突
  - 61.2 在尽量小的作用域中使用using namespace或者namespace a = " ";
- 六十二. C++的线程
  - 62.1 std::thread
- 六十三. C++的计时
  - 63.1 std::chrono
  - 63.2 特定平台下的高精度定时器(如win32 QueryPerformanceCounter)
  - 63.3 自定义struct Timer
  - 63.4 std::endl会刷新缓存区，可用‘\n’代替
- 六十四. C++多维数组
  - 64.1 int** a2d = new int*50
  - 64.2 注意二维数组delete时，需要调用两层delete
  - 64.3 实际上用一维数组模拟多维数组是最好的方法
- 六十五. C++的排序
  - 65.1 std::sort
- 六十六. C++的类型双关
  - 66.1 用不同的方式来解释同一片内存
  - 66.2 struct a{}; &a
- 六十七. C++的联合体(union)
  - 67.1 当想给同一个变量取两个不同的名字时，如(xyz)或(rgb)
  - 67.2
```
struct	Vector2 {
  float x, y;
};
struct Vector4 {
  union {
	  struct { float x, y, z, w;};
	  struct { Vector2 a, b; };
	};
};
```
- 六十八. C++的虚析构函数
  - 68.1 如果用基类指针来引用派生类对象，那么基类的析构函数必须是virtual的，否则C++只会调用基类的析构函数，不会调用派生类的析构函数
- 六十九. C++的类型转换
  - 69.1 C风格的强制类型转换
  - 69.2 static_cast 静态类型转换
  - 69.3 reinterpret_cast 类型双关(把某段内存重新解释成别的东西)
  - 69.4 dynamic_cast 不检查转换安全性，仅运行时检查，如果不能转换，返回null
  - 69.5 const_cast 移除或者添加变量的const限定
- 七十. 条件与操作断点
  - 70.1 调试模式下，鼠标右键断点->Conditions/Actions
- 七十一. 现代C++中的安全以及如何教授
- 七十二. C++的预编译头文件
  - 72.1 把经常用到且基本不会变化的头文件预编译(多用于不是自己写的代码)
  - 72.2 Tools->Options->Projects and Solutions->VC++ Project Settings->Build->Build Timing 查看编译时间
  - 72.3 Property->C/C++->Precompiled Headers->Precompiled Header(use) & Precompiled Header File(pch.h)
  - 72.4 pch.cpp Property->C/C++->Precompiled Headers->Precompiled Header(Create) & Precompiled Header File(pch.h)
- 七十三. C++的dynamic_cast
  - 73.1 常用来做多态类型转换验证，转换失败返回null指针
  - 73.2 Player *p0 = dynamic_cast<Player*>(actuallyPlayer)
  - 73.3 dynamic_cast只用于多态类类型
  - 73.4 RTTI 运行时类型识别
  - 73.5 Property->C/C++->Language->Enable Run-Time Type Information
  - 73.4 RTTI会有额外的性能开销
- 七十四. C++的基准测试
  - 74.1 在测试时间时，一点要确保确实做了这些事(例如release模式下会有优化，需要计时的代码可能被优化掉并未执行)
  - 74.2 确保是在release模式下测试时间
- 七十五. C++的结构化绑定(C++17)
  - 75.1 std::pair,std::tuple,std::tie
  - 75.2 Property->C/C++->Language->C++ Language Standard
  - 75.3 auto[name, age] = CreatorPerson; CreatorPerson返回值为tuple
  - 75.4 tie会将变量的引用整合成一个tuple，从而实现批量赋值
- 七十六. 如何处理Optional数据(C++17)
  - 76.1 使用场景—目标值可能存在也可能不存在，比如读取文件并返回内容，可能读取成功有数据，读取成功无数据，读取不成功
  - 76.2 has_value,value_or(xxx) 
- 七十七. 单一变量存放多种类型的数据(C++17)
  - 77.1 std::variant
  - 77.2 variant的大小是所有类型大小之和
  - 77.3 variant是一个类型安全的union
- 七十八. 如何存储任意类型的数据(C++17)
  - 78.1 std::any
  - 78.2 any相比variant不需要列出所有的类型
  - 78.3 any对于小类型来说，工作方式和variant完全相同。对于大类型，会进行动态分配(void *)
- 七十九. 如何让C++运行得更快
  - 79.1 并发(concurrency)：把任务在不同的时间点交给处理器进行处理。在同一时间点，任务并不会同时运行
  - 79.2 并行(parallelism)：把每一个任务分配给每一个处理器独立完成。在同一时间点，任务一定是同时运行
  - 79.3 std::asnyc, futures
  - 79.3 调试模式下->Debug->Windows->Parallel stacks
  - 79.4 std::async为什么一定要返回值-如果没有返回值，那么在一次for循环之后，临时对象会被析构，而析构函数中需要等待线程束，所以就和顺序执行一样，一个个的等下去如果将返回值赋值给外部变量，那么生存期就在for循环之外，那么对象不会被析构，也就不需要等待线程结束
  - 79.5 RAII
- 八十. 如何让C++字符串更快
  - 80.1 重载new运算符查看内存分配情况
  - 80.2 std::string_view(C++17)
- 八十一. C++的可视化基准测试
  - 81.1 chrome://tracing 
- 八十二. C++的单例模式
  - 82.1 单例模式的行为有点像命名空间 
  - 82.2 C++中的单例模式是一种组织一堆全局变量和静态函数的方式 
  - 82.3 学习cherno随机数生成器单例模式的代码
- 八十三. C++的小字符串优化
  - 83.1 string初始化时，任何小于15（不同编译器不同）个字符的字符串都不会导致堆分配
- 八十四. 跟踪内存分配的简单方法
  - 84.1 operator new
  - 84.2 operator delete
  - 84.3 定义一个struct记录申请和释放掉的内存
- 八十五. C++的左值与右值
  - 85.1 左值可以访问地址，没地址的是纯右值（临时值）
  - 85.2 函数参数为左值引用时，只接受左值，除非加上const
  - 85.3 函数参数为右值引用（&&）时，只接受右值
- 八十六. C++持续集成
  - 86.1 jenkins
- 八十七. C++静态分析
  - 87.1 pvs studio
- 八十八. C++的参数计算顺序
  - 88.1 未定义的行为
  - 88.2 C++17规定了参数求值必须一个接一个地完成，但仍未定义求值顺序
  - [88.3 多编译器代码测试网站Wandbox][5]
- 八十九. C++移动语义
  - 89.1 右值引用是左值
  - 89.2 std::move
  - 89.3 移动构造函数
  - [89.4 Cherno String的例子][7]
- 九十. std::move与移动赋值操作符
  - 90.1 赋值操作符，只有当我们把一个变量赋值给一个已有的变量时才会被调用
  - 90.2 default(C++11),减轻工作量和获得编译器自动生成的默认特殊成员函数的高的代码执行效率
  - 90.3 C++三法则：如果需要析构函数，则一定需要拷贝构造函数和拷贝赋值运算符。C++五法则：为了支持移动语义，又增加了移动构造函数和移动赋值运算符
  - [90.4 例子][7]
- 九十一. 自己写C++数据结构（Array）
- 九十二. 自己写C++数据结构（Vector）
- 九十九. 用C++编写桌面应用程序的最佳方法
  - 99.1 即时模式（immediate mode）会每次都重新绘制所有的元素，绝大多数游戏是这类模式
  - 99.2 保留模式（retain mode）当有需要改变的时候，执行的是改变的处理，绝大多数应用程序用的这种模式
  - [99.3 imgui][6]
- . [代码仓库][8]


[1]: https://www.bilibili.com/video/BV1uy4y167h2/
[2]: https://visualstudio.microsoft.com/
[3]: https://www.wholetomato.com/
[4]: https://www.asciitable.com/
[5]: https://wandbox.org/
[6]: https://github.com/ocornut/imgui/
[7]: https://www.cnblogs.com/zhangyi1357/p/16018810.html/
[8]: https://github.com/UrsoCN/NotesofCherno/
<!-- /code_chunk_output -->







