# 第六章 符号表管理技术  

## 概述  

1. 什么是符号表？  
   在编译过程中，编译程序用来记录源程序中各种名字的特性信息，所以也称为名字特性表。  

## 符号表的组织与内容  

1. 统一符号表——不论什么名字都填入统一格式的符号表中  
   符号表表项应按信息量最大的名字设计。填表、查表比较方便，结构简单，但是浪费大量空间。  
2. 对于不同种类的名字分别建立各种符号表  
   节省空间，但是填表和查表不方便。  

3. 折中办法——大部分共同信息组成统一格式的符号表。特殊信息另设附表，两者用指针连接。  

## 非分程序结构语言的符号表组织  

1. 非分程序的结构语言：  
   每个可独立进行编译的程序单元是一个不包含有子模块的单一模块。如FORTRAN语言。  
2. 标识符的作用域及基本处理办法  

## 分程序结构语言的符号表组织  

1. 分程序的结构语言： 模块内可嵌入子模块  
2. 标识符的作用域和基本处理方法 
    建查符号表均要遵循标识符作用域规定进行。建表不能重复，不能遗漏。查表要按标识符作用域查找。  

### 分程序符号表的组织方式  

1. 分层组织符号表的登记项  
    各分程序符号表登记项按照语法识别顺序连续裴烈在一起，不为其内层分程序的符号表登记项所割裂。  
2. 用“分程序表”索引各分程序符号表的信息  
   分程序表中的各登记项是自左至右扫描源程序的过程中，按分程序出现的顺序依次填入的，且对每一个分程序填写一个登记项。分程序表登记项序号隐含地表征各分程序的编号。

#### 要求会画出栈式符号表  
