
# GV5 SDK C++规范

## 1.1. 代码规范
* 类名称如果重复的概率比较大，用命名空间包含，否则静态生成很容易冲突
* 基类要求虚析构函数
* 子类重载虚函数，加virutal + override
* 文件头的宏格式,GEOVIS_+库名称+文件名称，如GEOVIS_CORE_MAP_H
* 头文件尽量只包含声明，将实现放到Cpp中
* 多用命名空间格式
``` 
Namespace GeoVIS{ namespace Core{
}} 
```
* 取值函数用const后缀装饰
 ``` 
int size() const;
``` 
* 函数、变量等采用小驼峰命名,第一个字母小写，后面大写,
```  std::string filePath ``` 
* 类名称采用第一个字母大写
* 类成员变量，采用_+变量名
``` 
int fileSize
void onResize();
``` 
* 局部变量，不要加
* 头文件尽量用声明，不去包含头文件，将包含留到c++中
```
#include 
class Test
{
    private:
    MyClass* _obj;
}
``` 
``` 
class MyClass;
class Test{
    private:
    MyClass* _obj;
}
``` 
* 所提交代码尽量无warning，必须无error
* float变量赋值，加f,``` float red = 0.5f;``` 
* 类成员尽量采用参数初始化，而非赋值；指针必须进行初始化
``` 
Map::Map()
:_view(NULL)
{
}
``` 
* 对于复合类型，尽量const &避免直接用类型，避免类型拷贝带来的代价
* 不使用：IGV_Map* getMap(std::string name);
* 使用：IGV_Map* getMap(const std::string& name);

## 1.2. 命名规范
* 工程相关目录，采用大写方式比,如:GVUtil
* 配置相关文件夹名称，小写+_,如:bin,work_dir
* 除了代码相关的文件名称大小，其他全部小写
* 如果外部可使用的头文件，头文件跟实现文件分开放置
* Enum定义方式,参考
``` 
enum RenderType
{
    RT_Thread,
    RT_MultiThread
};
``` 
* 接口文件名称，IGV_接口名称

## 1.3. 文件引用规范
* 注意 ""跟<>区别，内部使用””，已经引用到工作目录的用<>
* 头文件包含顺序,先标准库，后内部库；类似osg方式包含
* 库引用、生成规范；
* 用引用目录+库名称方式
* Debug库加d
* 文件目录引用

## 1.4. 注释规范
* 除了接口文件，不用中文
* cpp类之间分割``` //className----------------------``` 
* 文件头必须注释
* 接口需要注释
