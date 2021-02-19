
Speicherklasse:
static,extern,register,mutable

extern:
一个文件里的全局变量，在其他的文件里也可以访问，但是必须在这个其他文件里面先用extern声明下。
static:
可以用匿名namespace限定全局变量的编译，就是说只能在一个文件里被访问。

但是如果是常量，constant, 全局常量只能在本地文件访问，如果需要在别的文件访问，需要定义为extern const。别的文件里也需要声明extern const

register:
因为速度原因告诉CPU放在寄存器里

头文件里面的全局变量可能会被多个文件引用而造成错误

3.3.5 Compilerdirektiven und Makros

template function
编译器会根据需要生成所需要的各个function.

特殊情况具体设计的template

template<>
bool kleiner<int>(const int& a, const int& b)
  {...}
  
也可以用函数重载，但是函数重载有隐形类型转换的问题

inline程序，应该在头文件里
