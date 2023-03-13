# Java基础

## 一、简介
Java是由Sun Microsystem公司于1995年5月推出的Java面向对象程序设计语言和Java平台的总称。由James Gosling和同事们共同研发，并在1995年正式推出。

Java分为三个体系：
* JavaSE(J2SE) (Java2 Platform Standard Edition, java平台标准版）
* JavaEE(J2EE) (Java2 Platform,Enterprise Edition, java平台企业版）
* JavaME(J2ME) (Java2 Platform Micro Edition, java平台微型版）

## 二、面向对象
Java 是面向对象的高级编程语言，类和对象是 Java 程序的构成核心。Java语言提供类，接口和继承等面向对象特性，为了简单起见，只支持类之间的单继承，但支持接口间的多继承，并支持类与接口之间的实现机制。面向对象是一种常见的思想，比较符合人们的思考习惯；面向对象可以将复杂的业务逻辑简单化，增强代码复用性。从理论上讲，只要对象能够实现业务功能，其具体的实现细节不必特别关心。
围绕着 Java 类和 Java 对象，有三大基本特性：

* **封装（Java 类的编写规范）**
* **继承（类与类之间联系的一种形式）**
* **多态（为系统组件或模块之间解耦提供了解决方案）**

现实世界中，随处可见的一种事物就是对象，对象是事物存在的实体，如人类、书桌、计算机、高楼大厦等。人类解决问题的方式总是将复杂的事物简单化，于是就会思考这些对象都是由哪些部分组成的。通常都会将对象划分为两个部分，即动态部分与静态部分。 静态部分，顾名思义就是不能动的部分，这个部分被称为“属性”，任何对象都会具备其自身属性，如一个人，它包括高矮、胖瘦、性别、年龄等属性。然而具有这些属性的人会执行哪些动作也是一个值得探讨的部分，这个人可以哭泣、微笑、说话、行走，这些是这个人具备的行为（动态部分）即方法，人类通过探讨对象的属性和观察对象的行为了解对象。

面向对象编程是当今主流的程序设计思想，已经取代了过程化程序开发技术。

## 三、基本数据类型
变量就是申请内存来存储值。也就是说，当创建变量的时候，需要在内存中申请空间。内存管理系统根据变量的类型为变量分配存储空间，分配的空间只能用来储存该类型数据。Java 的两大数据类型:

* **内置数据类型**
* **引用数据类型**

### 1.内置数据类型

* **byte**

	byte数据类型是8位、有符号的, 默认值为0.
* **short**

	short数据类型是16位、有符号的, 默认值为0.
* **int**

	int数据类型是32位、有符号的, 默认值为0.
* **long**

	long数据类型是64位、有符号的, 默认值为0L.
* **float**

	float 数据类型是单精度、32位、符合IEEE 754标准的浮点数, 默认值0.0f.
* **double**

	double 数据类型是双精度、64 位、符合 IEEE 754 标准的浮点数， 默认值0.0d.
* **boolean**

	boolean数据类型表示一位的信息；只有两个取值：true 和 false；默认值是 false；

* **char**

	char 类型是一个单一的 16 位 Unicode 字符；最小值是 \u0000（十进制等效值为 0）；最大值是 \uffff（即为 65535）；char 数据类型可以储存任何字符；默认值'\u0000'.

| **数据类型**           | **默认值** |
| :--------------------- | :--------- |
| byte                   | 0          |
| short                  | 0          |
| int                    | 0          |
| long                   | 0L         |
| float                  | 0.0f       |
| double                 | 0.0d       |
| char                   | 'u0000'    |
| String (or any object) | null       |
| boolean                | false      |



Java语言支持一些特殊的转义字符序列。

| 符号   | 字符含义                 |
| :----- | :----------------------- |
| \n     | 换行 (0x0a)              |
| \r     | 回车 (0x0d)              |
| \f     | 换页符(0x0c)             |
| \b     | 退格 (0x08)              |
| \0     | 空字符 (0x0)             |
| \s     | 空格 (0x20)              |
| \t     | 制表符                   |
| \"     | 双引号                   |
| \'     | 单引号                   |
| \\     | 反斜杠                   |
| \ddd   | 八进制字符 (ddd)         |
| \uxxxx | 16进制Unicode字符 (xxxx) |

 

**自动类型转换：**
	
*整型、实型（常量）、字符型数据可以混合运算。运算中，不同类型的数据先转化为同一类型，然后进行运算。转换从低级到高级。*
*byte,short,char—> int —> long—> float —> double*

**强制类型转换：**

*条件是转换的数据类型必须是兼容的。格式：(type)value type是要强制类型转换后的数据类型。*

### 2.引用数据类型

在Java中，引用类型的变量非常类似于C/C++的指针。引用类型指向一个对象，指向对象的变量是引用变量。这些变量在声明时被指定为一个特定的类型，比如 Employee、Puppy 等。变量一旦声明后，类型就不能被改变了。对象、数组都是引用数据类型。所有引用类型的默认值都是null。一个引用变量可以用来引用任何与之兼容的类型。

## 四、修饰符

Java语言提供了很多修饰符，主要分为以下两类：

- 访问控制修饰符
- 非访问控制修饰符

### 1.访问控制修饰符

Java中，可以使用访问控制符来保护对类、变量、方法和构造方法的访问。Java 支持 4 种不同的访问权限。

- **default** (即默认，什么也不写）: 在同一包内可见，不使用任何修饰符。使用对象：类、接口、变量、方法。
- **private** : 在同一类内可见。使用对象：变量、方法。 **注意：不能修饰类（外部类）**
- **public** : 对所有类可见。使用对象：类、接口、变量、方法
- **protected** : 对同一包内的类和所有子类可见。使用对象：变量、方法。 **注意：不能修饰类（外部类）**。

| 修饰符      | 当前类 | 同一包内 | 子孙类(同一包) | 子孙类(不同包) | 其他包 |
| :---------- | :----- | :------- | :------------- | :------------- | :----- |
| `public`    | Y      | Y        | Y              | Y              | Y      |
| `protected` | Y      | Y        | Y              | Y/N            | N      |
| `default`   | Y      | Y        | Y              | N              | N      |
| `private`   | Y      | N        | N              | N              | N      |



**访问控制和继承的规则：**

- 父类中声明为 public 的方法在子类中也必须为 public。
- 父类中声明为 protected 的方法在子类中要么声明为 protected，要么声明为 public，不能声明为 private。
- 父类中声明为 private 的方法，不能够被子类继承。

### 2.非访问控制修饰符

为了实现一些其他的功能，Java 也提供了许多非访问修饰符。

* **static** 修饰符，用来修饰类方法和类变量。

* **final** 修饰符，用来修饰类、方法和变量，final 修饰的类不能够被继承，修饰的方法不能被继承类重新定义，修饰的变量为常量，是不可修改的。

* **abstract** 修饰符，用来创建抽象类和抽象方法。

* **synchronized** 修饰符，声明的方法同一时间只能被一个线程访问。

* **volatile** 修饰符，修饰的成员变量在每次被线程访问时，都强制从共享内存中重新读取该成员变量的值。而且，当成员变量发生变化时，会强制线程将变化值回写到共享内存。这样在任何时刻，两个不同的线程总是看到某个成员变量的同一个值。一个 volatile 对象引用可能是 null。

  ```java
  public class MyRunnable implements Runnable
  {
      private volatile boolean active;
      public void run()
      {
          active = true;
          while (active) // 第一行
          {
              // 代码
          }
      }
      public void stop()
      {
          active = false; // 第二行
      }
  }
  ```

  通常情况下，在一个线程调用 run() 方法（在 Runnable 开启的线程），在另一个线程调用 stop() 方法。 如果 ***第一行\*** 中缓冲区的 active 值被使用，那么在 ***第二行\*** 的 active 值为 false 时循环不会停止。但是以上代码中我们使用了 volatile 修饰 active，所以该循环会停止。

* **transient** 修饰符，序列化的对象包含被 transient 修饰的实例变量时，java 虚拟机(JVM)跳过该特定的变量。该修饰符包含在定义变量的语句中，用来预处理类和变量的数据类型。

  ```java
  public transient int limit = 55;   // 不会持久化
  public int b; // 持久化
  ```

  

## 五、String及其包装类

### 1.字符串创建

在 Java 中字符串属于对象，Java 提供了 String 类来创建和操作字符串。String直接创建的字符串存储在公共池（字符串常量池）中，而 new 创建的字符串对象在堆上：

```java
String s1 = "Runoob";              // String 直接创建
String s2 = "Runoob";              // String 直接创建
String s3 = s1;                    // 相同引用
String s4 = new String("Runoob");   // String 对象创建
String s5 = new String("Runoob");   // String 对象创建
```

![字符串内存模型][java-string]

String创建之后是不可修改的，这点是是基于代码封装和访问控制实现的。从String源码可以看见，String类用final关键字修饰，意味着String类不能被继承；它的成员方法都默认为final方法；String实例的值是通过字符数组实现字符串存储的，内部成员char数组final修饰的，字符串一旦创建就不能再修改；虽然char数组本身的值可以改变（即修改的是数组上每一个元素本身的值，而并未修改数组，不违反final关键字定义），但是String内部并未提供这一方法。因此String不可变是基于代码封装和访问控制实现的。当对字符串进行修改的时候，需要使用 StringBuffer 和 StringBuilder 类。



### 2.字符串连接

* **concat方法**

  ```java
  string1.concat(string2);
  ```

  

* **+**

  ```java
  "Hello," + " runoob" + "!"
  ```

  字符串进行加号（+）运算，最终得到是一个拼接的新的字符串。然后调用toString（）把拼接的对象转换成字符串对象，最后把得到字符串对象的地址赋值给变量。“+”连接符的本质是通过StringBuilder实现的，使用“+”连接符大量循环拼接字符串时，会隐式地创建多次StringBuilder对象，造成浪费及效率的损失，则应直接使用StringBuilder/StringBuffer进行创建。

### 3.字符串常量池

在Java的内存分配中，总共3种常量池，分别是Class常量池、运行时常量池、全局字符串池（字符串常量池）。

为了提高性能并减少内存的开销，JVM在实例化字符串常量时进行了一系列的优化操作：

* 在JVM层面为字符串提供字符串常量池，可以理解为是一个缓存区；

* 创建字符串常量时，JVM会检查字符串常量池中是否存在这个字符串；

* 若字符串常量池中存在该字符串，则直接返回引用实例；若不存在，先实例化该字符串，并且，将该字符串放入字符串常量池中，以便于下次使用时，直接取用，达到缓存快速使用的效果。

* 由于String字符串的不可变性，常量池中一定不存在两个相同的字符串。

**在HotSpot VM中字符串常量池是通过一个StringTable类实现的**，它是一个Hash表，默认值大小长度是1009；这个StringTable在每个HotSpot VM的实例中只有一份，被所有的类共享；字符串常量由一个一个字符组成，放在了StringTable上。要注意的是，如果放进String Pool的String非常多，就会造成Hash冲突严重，从而导致链表会很长，而链表长了后直接会造成的影响就是当调用String.intern时性能会大幅下降（因为要一个一个找）。

在jdk1.7之前，常量池是存放在方法区中的。在jdk1.7中，字符串常量池移到了堆中，运行时常量池还在方法区中。

### 4.StringBuffer和StringBuilder

和 String 类不同的是，StringBuffer 和 StringBuilder 类的对象能够被多次的修改，并且不产生新的未使用对象。在使用 StringBuffer 类时，每次都会对 StringBuffer 对象本身进行操作，而不是生成新的对象，所以如果需要对字符串进行修改推荐使用 StringBuffer。StringBuilder 类在 Java 5 中被提出，它和 StringBuffer 之间的最大不同在于 StringBuilder 的方法不是线程安全的（不能同步访问）。由于 StringBuilder 相较于 StringBuffer 有速度优势，所以多数情况下建议使用 StringBuilder 类。而在应用程序要求线程安全的情况下，则必须使用 StringBuffer 类。

​	![字符串工具][java-string1]



在append方法中，当字符串长度不足时，扩容为原字符串长度加新字符串长度，若长度超过jvm支持的最大数组长度MAX_ARRAY_SIZE则抛出异常。StringBuffer和StringBuilder的append方法的不同在于前者有synchronized修饰符是线程安全而后者则没有是线程不安全的。

## 六、正则表达式

java.util.regex 包主要包括以下三个类：

- Pattern 类：

  pattern 对象是一个正则表达式的编译表示。Pattern 类没有公共构造方法。要创建一个 Pattern 对象，你必须首先调用其公共静态编译方法，它返回一个 Pattern 对象。该方法接受一个正则表达式作为它的第一个参数。

- Matcher 类：

  Matcher 对象是对输入字符串进行解释和匹配操作的引擎。与Pattern 类一样，Matcher 也没有公共构造方法。你需要调用 Pattern 对象的 matcher 方法来获得一个 Matcher 对象。

- PatternSyntaxException：

  PatternSyntaxException 是一个非强制异常类，它表示一个正则表达式模式中的语法错误。

| 字符          | 说明                                                         |
| :------------ | :----------------------------------------------------------- |
| \             | 将下一字符标记为特殊字符、文本、反向引用或八进制转义符。例如， **n**匹配字符 **n**。**\n** 匹配换行符。序列 **\\\\** 匹配 **\\** ，**\\(** 匹配 **(**。 |
| ^             | 匹配输入字符串开始的位置。如果设置了 **RegExp** 对象的 **Multiline** 属性，^ 还会与"\n"或"\r"之后的位置匹配。 |
| $             | 匹配输入字符串结尾的位置。如果设置了 **RegExp** 对象的 **Multiline** 属性，$ 还会与"\n"或"\r"之前的位置匹配。 |
| *             | 零次或多次匹配前面的字符或子表达式。例如，zo* 匹配"z"和"zoo"。* 等效于 {0,}。 |
| +             | 一次或多次匹配前面的字符或子表达式。例如，"zo+"与"zo"和"zoo"匹配，但与"z"不匹配。+ 等效于 {1,}。 |
| ?             | 零次或一次匹配前面的字符或子表达式。例如，"do(es)?"匹配"do"或"does"中的"do"。? 等效于 {0,1}。 |
| {*n*}         | *n* 是非负整数。正好匹配 *n* 次。例如，"o{2}"与"Bob"中的"o"不匹配，但与"food"中的两个"o"匹配。 |
| {*n*,}        | *n* 是非负整数。至少匹配 *n* 次。例如，"o{2,}"不匹配"Bob"中的"o"，而匹配"foooood"中的所有 o。"o{1,}"等效于"o+"。"o{0,}"等效于"o*"。 |
| {*n*,*m*}     | *m* 和 *n* 是非负整数，其中 *n* <= *m*。匹配至少 *n* 次，至多 *m* 次。例如，"o{1,3}"匹配"fooooood"中的头三个 o。'o{0,1}' 等效于 'o?'。注意：您不能将空格插入逗号和数字之间。 |
| ?             | 当此字符紧随任何其他限定符（*、+、?、{*n*}、{*n*,}、{*n*,*m*}）之后时，匹配模式是"非贪心的"。"非贪心的"模式匹配搜索到的、尽可能短的字符串，而默认的"贪心的"模式匹配搜索到的、尽可能长的字符串。例如，在字符串"oooo"中，"o+?"只匹配单个"o"，而"o+"匹配所有"o"。 |
| .             | 匹配除"\r\n"之外的任何单个字符。若要匹配包括"\r\n"在内的任意字符，请使用诸如"[\s\S]"之类的模式。 |
| (*pattern*)   | 匹配 *pattern* 并捕获该匹配的子表达式。可以使用 **$0…$9** 属性从结果"匹配"集合中检索捕获的匹配。若要匹配括号字符 ( )，请使用"\("或者"\)"。 |
| (?:*pattern*) | 匹配 *pattern* 但不捕获该匹配的子表达式，即它是一个非捕获匹配，不存储供以后使用的匹配。这对于用"or"字符 (\|) 组合模式部件的情况很有用。例如，'industr(?:y\|ies) 是比 'industry\|industries' 更经济的表达式。 |
| (?=*pattern*) | 执行正向预测先行搜索的子表达式，该表达式匹配处于匹配 *pattern* 的字符串的起始点的字符串。它是一个非捕获匹配，即不能捕获供以后使用的匹配。例如，'Windows (?=95\|98\|NT\|2000)' 匹配"Windows 2000"中的"Windows"，但不匹配"Windows 3.1"中的"Windows"。预测先行不占用字符，即发生匹配后，下一匹配的搜索紧随上一匹配之后，而不是在组成预测先行的字符后。 |
| (?!*pattern*) | 执行反向预测先行搜索的子表达式，该表达式匹配不处于匹配 *pattern* 的字符串的起始点的搜索字符串。它是一个非捕获匹配，即不能捕获供以后使用的匹配。例如，'Windows (?!95\|98\|NT\|2000)' 匹配"Windows 3.1"中的 "Windows"，但不匹配"Windows 2000"中的"Windows"。预测先行不占用字符，即发生匹配后，下一匹配的搜索紧随上一匹配之后，而不是在组成预测先行的字符后。 |
| *x*\|*y*      | 匹配 *x* 或 *y*。例如，'z\|food' 匹配"z"或"food"。'(z\|f)ood' 匹配"zood"或"food"。 |
| [*xyz*]       | 字符集。匹配包含的任一字符。例如，"[abc]"匹配"plain"中的"a"。 |
| [^*xyz*]      | 反向字符集。匹配未包含的任何字符。例如，"[^abc]"匹配"plain"中"p"，"l"，"i"，"n"。 |
| [*a-z*]       | 字符范围。匹配指定范围内的任何字符。例如，"[a-z]"匹配"a"到"z"范围内的任何小写字母。 |
| [^*a-z*]      | 反向范围字符。匹配不在指定的范围内的任何字符。例如，"[^a-z]"匹配任何不在"a"到"z"范围内的任何字符。 |
| \b            | 匹配一个字边界，即字与空格间的位置。例如，"er\b"匹配"never"中的"er"，但不匹配"verb"中的"er"。 |
| \B            | 非字边界匹配。"er\B"匹配"verb"中的"er"，但不匹配"never"中的"er"。 |
| \c*x*         | 匹配 *x* 指示的控制字符。例如，\cM 匹配 Control-M 或回车符。*x* 的值必须在 A-Z 或 a-z 之间。如果不是这样，则假定 c 就是"c"字符本身。 |
| \d            | 数字字符匹配。等效于 [0-9]。                                 |
| \D            | 非数字字符匹配。等效于 [^0-9]。                              |
| \f            | 换页符匹配。等效于 \x0c 和 \cL。                             |
| \n            | 换行符匹配。等效于 \x0a 和 \cJ。                             |
| \r            | 匹配一个回车符。等效于 \x0d 和 \cM。                         |
| \s            | 匹配任何空白字符，包括空格、制表符、换页符等。与 [ \f\n\r\t\v] 等效。 |
| \S            | 匹配任何非空白字符。与 [^ \f\n\r\t\v] 等效。                 |
| \t            | 制表符匹配。与 \x09 和 \cI 等效。                            |
| \v            | 垂直制表符匹配。与 \x0b 和 \cK 等效。                        |
| \w            | 匹配任何字类字符，包括下划线。与"[A-Za-z0-9_]"等效。         |
| \W            | 与任何非单词字符匹配。与"[^A-Za-z0-9_]"等效。                |
| \x*n*         | 匹配 *n*，此处的 *n* 是一个十六进制转义码。十六进制转义码必须正好是两位数长。例如，"\x41"匹配"A"。"\x041"与"\x04"&"1"等效。允许在正则表达式中使用 ASCII 代码。 |
| \*num*        | 匹配 *num*，此处的 *num* 是一个正整数。到捕获匹配的反向引用。例如，"(.)\1"匹配两个连续的相同字符。 |
| \*n*          | 标识一个八进制转义码或反向引用。如果 \*n* 前面至少有 *n* 个捕获子表达式，那么 *n* 是反向引用。否则，如果 *n* 是八进制数 (0-7)，那么 *n* 是八进制转义码。 |
| \*nm*         | 标识一个八进制转义码或反向引用。如果 \*nm* 前面至少有 *nm* 个捕获子表达式，那么 *nm* 是反向引用。如果 \*nm* 前面至少有 *n* 个捕获，则 *n* 是反向引用，后面跟有字符 *m*。如果两种前面的情况都不存在，则 \*nm* 匹配八进制值 *nm*，其中 *n* 和 *m*是八进制数字 (0-7)。 |
| \nml          | 当 *n* 是八进制数 (0-3)，*m* 和 *l* 是八进制数 (0-7) 时，匹配八进制转义码 *nml*。 |
| \u*n*         | 匹配 *n*，其中 *n* 是以四位十六进制数表示的 Unicode 字符。例如，\u00A9 匹配版权符号 (©)。 |



## 七、包

为了更好地组织类，Java 提供了包机制，用于区别类名的命名空间。包的作用：

- 1、把功能相似或相关的类或接口组织在同一个包中，方便类的查找和使用。
- 2、如同文件夹一样，包也采用了树形目录的存储方式。同一个包中的类名字是不同的，不同的包中的类的名字是可以相同的，当同时调用两个不同包中相同类名的类时，应该加上包名加以区别。因此，包可以避免名字冲突。
- 3、包也限定了访问权限，拥有包访问权限的类才能访问某个包中的类。

Java 使用包（package）这种机制是为了防止命名冲突，访问控制，提供搜索和定位。

### 1.package 

包声明应该在源文件的第一行，每个源文件只能有一个包声明，这个文件中的每个类型都应用于它。

```java
/* 文件名: Animal.java */
package animals;
 
interface Animal {
   public void eat();
   public void travel();
}
```



### 2.import

为了能够使用某一个包的成员，我们需要在 Java 程序中明确导入该包。使用 "import" 语句可完成此功能。

```java
import payroll.*;
```





## 八、类和接口

### 1.类

对某类事物的普遍一致性特征和功能的抽象描述和封装，是构造对象的模板或蓝图。类之间主要有：依赖，聚合，继承等关系。在Java中类文件包含：包管理、类声明、属性、构造方法和类方法。

#### 类声明 

通过***class***关键字声明类。例如：

```java
import java.io.*;//包管理
 
public class Employee{//类声明
   String name;
   int age;
   String designation;
   double salary;
   // Employee 类的构造器
   public Employee(String name){
      this.name = name;
   }
   // 设置age的值
   public void empAge(int empAge){
      age =  empAge;
   }
   /* 设置designation的值*/
   public void empDesignation(String empDesig){
      designation = empDesig;
   }
   /* 设置salary的值*/
   public void empSalary(double empSalary){
      salary = empSalary;
   }
   /* 打印信息 */
   public void printEmployee(){
      System.out.println("名字:"+ name );
      System.out.println("年龄:" + age );
      System.out.println("职位:" + designation );
      System.out.println("薪水:" + salary);
   }
}
```

#### 类继承

***Java只支持类之间的单继承，但支持多重继承。子类继承父类，同时拥有父类对子类公开的属性和方法。***

![][java-extends]

在Java中通过***extends***关键字来声明继承关系的，例如：

```java
public class Animal { 
    private String name;   
    private int id; 
    public Animal(String myName, int myid) { 
        //初始化属性值
    } 
    public void eat() {  //吃东西方法的具体实现  } 
    public void sleep() { //睡觉方法的具体实现  } 
} 
 
public class Penguin  extends  Animal{ 
}
```



### 2.抽象类

在Java中使用abstract来声明抽象类。抽象类不能被实例化，必须通过子类实现才能被使用。因为抽象类必须有子类所以不能使用final修饰符。在抽象类中使用abstract声明的抽象方法没有方法体，子类继承抽象类强制必须实现这些抽象方法，除非子类也是抽象类。抽象类通常用来封装一些公共属性和方法。抽象类中不一定包含抽象方法，但是有抽象方法的类必定是抽象类。

```java
public abstract class Employee
{
   private String name;
   private String address;
   private int number;
   
   public abstract double computePay();
   
   //其余代码
}
```



### 3.接口

接口（英文：Interface），在JAVA编程语言中是一个抽象类型，是抽象方法的集合，接口以interface来声明。一个类通过实现接口的方式，从而来实现接口的抽象方法。接口并不是类，编写接口的方式和类很相似，但是它们属于不同的概念。类描述对象的属性和方法。接口则包含类要实现的方法。除非实现接口的类是抽象类，否则该类要实现接口中的所有方法。

#### 接口特性

- 接口中每一个方法也是隐式抽象的,接口中的方法会被隐式的指定为 **public abstract**（只能是 public abstract，其他修饰符都会报错）。
- 接口中可以含有变量，但是接口中的变量会被隐式的指定为 **public static final** 变量（并且只能是 public，用 private 修饰会报编译错误）。
- 接口中的方法是不能在接口中实现的，只能由实现接口的类来实现接口中的方法。



```java
/* 文件名 : Animal.java */
interface Animal {
   public void eat();
   public void travel();
}
```

#### 抽象类和接口的区别

- 抽象类中的方法可以有方法体，就是能实现方法的具体功能，但是接口中的方法不行。
- 抽象类中的成员变量可以是各种类型的，而接口中的成员变量只能是 **public static final** 类型的。
- 接口中不能含有静态代码块以及静态方法(用 static 修饰的方法)，而抽象类是可以有静态代码块和静态方法。
- 一个类只能继承一个抽象类，而一个类却可以实现多个接口。

**注**：JDK 1.8 以后，接口里可以有静态方法和方法体了。

**注**：JDK 1.8 以后，接口允许包含具体实现的方法，该方法称为"默认方法"，默认方法使用 default 关键字修饰。

**注**：JDK 1.9 以后，允许将方法定义为 private，使得某些复用的代码不会把方法暴露出去。

#### 标记接口

标记接口是没有任何方法和属性的接口.它仅仅表明它的类属于一个特定的类型,供其他代码来测试允许做一些事情。标记接口作用：简单形象的说就是给某个对象打个标签，使对象拥有某个或某些特权。标记接口主要用于以下两种目的：

- 建立一个公共的父接口：

  正如EventListener接口，这是由几十个其他接口扩展的Java API，你可以使用一个标记接口来建立一组接口的父接口。例如：当一个接口继承了EventListener接口，Java虚拟机(JVM)就知道该接口将要被用于一个事件的代理方案。

- 向一个类添加数据类型：

  这种情况是标记接口最初的目的，实现标记接口的类不需要定义任何接口方法(因为标记接口根本就没有方法)，但是该类通过多态性变成一个接口类型。

#### 接口的继承

在Java中，类的多继承是不合法，但接口允许多继承。在接口的多继承中extends关键字只需要使用一次，在其后跟着继承接口。

```java
public interface Hockey extends Sports, Event
```



#### 接口实现

在Java中通过***implements***关键字来声明类实现了某个接口的，同一个类可以实现多个接口。

例如：

```java
/* 文件名 : MammalInt.java */
public class MammalInt implements Animal{
 
   public void eat(){
      System.out.println("Mammal eats");
   }
 
   public void travel(){
      System.out.println("Mammal travels");
   } 
 
   public int numOfLegs(){
      return 0;
   }
 
   public static void main(String args[]){
      MammalInt m = new MammalInt();
      m.eat();
      m.travel();
   }
}
```



### 4.封装

在面向对象程式设计方法中，封装（英语：Encapsulation）是指一种将抽象性函式接口的实现细节部分包装、隐藏起来的方法。封装可以被认为是一个保护屏障，防止该类的代码和数据被外部类定义的代码随机访问。要访问该类的代码和数据，必须通过严格的接口控制。将对象不需要让外界访问的成员变量和方法私有化，只提供符合开发者意愿的公共方法来访问这些数据和逻辑，保证了数据的安全和程序的稳定。封装以隐藏细节、数据安全和程序稳定为目的。

**封装的优点**

- 良好的封装能够减少耦合。
- 类内部的结构可以自由修改。
- 可以对成员变量进行更精确的控制。
- 隐藏信息和实现细节。

***封装其实就是通过修改属性或方法的可见性即修饰符来限制外部的访问权限，只提供符合开发者意愿的公共方法来访问这些数据和逻辑。***

### 5.方法重写重载与多态

#### 重写（Override）

重写是子类对父类的允许访问的方法的实现过程进行重新编写, 返回值和形参都不能改变。重写方法不能抛出新的检查异常或者比被重写方法申明更加宽泛的异常。例如： 父类的一个方法申明了一个检查异常 IOException，但是在重写这个方法的时候不能抛出 Exception 异常，因为 Exception 是 IOException 的父类，抛出 IOException 异常或者 IOException 的子类异常。重写的好处在于子类可以根据需要，定义特定于自己的行为。 也就是说子类能够根据需要实现父类的方法。在运行时，Java 虚拟机(JVM)指定对象的类型并且运行该对象的方法。

```java
class Animal{
   public void move(){
      System.out.println("动物可以移动");
   }
}
 
class Dog extends Animal{
   public void move(){
      System.out.println("狗可以跑和走");
   }
}
 
public class TestDog{
   public static void main(String args[]){
      Animal a = new Animal(); // Animal 对象
      Animal b = new Dog(); // Dog 对象
 
      a.move();// 执行 Animal 类的方法
 
      b.move();//执行 Dog 类的方法
   }
}
```

**方法的重写规则**

- 参数列表与被重写方法的参数列表必须完全相同。
- 返回类型与被重写方法的返回类型可以不相同，但是必须是父类返回值的派生类（java5 及更早版本返回类型要一样，java7 及更高版本可以不同）。
- 访问权限不能比父类中被重写的方法的访问权限更低。例如：如果父类的一个方法被声明为 public，那么在子类中重写该方法就不能声明为 protected。
- 父类的成员方法只能被它的子类重写。
- 声明为 final 的方法不能被重写。
- 声明为 static 的方法不能被重写，但是能够被再次声明。
- 子类和父类在同一个包中，那么子类可以重写父类所有方法，除了声明为 private 和 final 的方法。
- 子类和父类不在同一个包中，那么子类只能够重写父类的声明为 public 和 protected 的非 final 方法。
- 重写的方法能够抛出任何非强制异常，无论被重写的方法是否抛出异常。但是，重写的方法不能抛出新的强制性异常，或者比被重写方法声明的更广泛的强制性异常，反之则可以。
- 构造方法不能被重写。
- 如果不能继承一个类，则不能重写该类的方法。

#### super关键字

当需要在子类中调用父类的被重写方法时，要使用 super 关键字。

```java
class Animal{
   public void move(){
      System.out.println("动物可以移动");
   }
}
 
class Dog extends Animal{
   public void move(){
      super.move(); // 应用super类的方法
      System.out.println("狗可以跑和走");
   }
}
 
public class TestDog{
   public static void main(String args[]){
 
      Animal b = new Dog(); // Dog 对象
      b.move(); //执行 Dog类的方法
 
   }
}
```



#### 重载（Overload）

重载(overloading) 是在一个类里面，方法名字相同，而参数不同。返回类型可以相同也可以不同。每个重载的方法（或者构造函数）都必须有一个独一无二的参数类型列表。最常用的地方就是构造器的重载。

**重载规则:**

- 被重载的方法必须改变参数列表(参数个数或类型不一样)；
- 被重载的方法可以改变返回类型；
- 被重载的方法可以改变访问修饰符；
- 被重载的方法可以声明新的或更广的检查异常；
- 方法能够在同一个类中或者在一个子类中被重载。
- 无法以返回值类型作为重载函数的区分标准。

```java
public class Overloading {
    public int test(){
        System.out.println("test1");
        return 1;
    }
 
    public void test(int a){
        System.out.println("test2");
    }   
 
    //以下两个参数类型顺序不同
    public String test(int a,String s){
        System.out.println("test3");
        return "returntest3";
    }   
 
    public String test(String s,int a){
        System.out.println("test4");
        return "returntest4";
    }   
 
    public static void main(String[] args){
        Overloading o = new Overloading();
        System.out.println(o.test());
        o.test(1);
        System.out.println(o.test(1,"test3"));
        System.out.println(o.test("test4",1));
    }
}
```



#### 多态

多态是同一个行为具有多个不同表现形式或形态的能力。当使用多态方式调用方法时，首先检查父类中是否有该方法，如果没有，则编译错误；如果有，再去调用子类的同名方法。

![多态][java-duotai]

**多态的优点**

- 消除类型之间的耦合关系
- 可替换性
- 可扩充性
- 接口性
- 灵活性
- 简化性

**多态的实现方式**

* 重写

  子类重写父类的方法，父类引用指向子类对象，实际调用时执行的是子类中的方法。

* 接口

* 抽象类和抽象方法

```java
public class Test {
    public static void main(String[] args) {
      show(new Cat());  // 以 Cat 对象调用 show 方法
      show(new Dog());  // 以 Dog 对象调用 show 方法
                
      Animal a = new Cat();  // 向上转型  
      a.eat();               // 调用的是 Cat 的 eat
      Cat c = (Cat)a;        // 向下转型  
      c.work();        // 调用的是 Cat 的 work
  }  
            
    public static void show(Animal a)  {
      a.eat();  
        // 类型判断
        if (a instanceof Cat)  {  // 猫做的事情 
            Cat c = (Cat)a;  
            c.work();  
        } else if (a instanceof Dog) { // 狗做的事情 
            Dog c = (Dog)a;  
            c.work();  
        }  
    }  
}
 
abstract class Animal {  
    abstract void eat();  
}  
  
class Cat extends Animal {  
    public void eat() {  
        System.out.println("吃鱼");  
    }  
    public void work() {  
        System.out.println("抓老鼠");  
    }  
}  
  
class Dog extends Animal {  
    public void eat() {  
        System.out.println("吃骨头");  
    }  
    public void work() {  
        System.out.println("看家");  
    }  
}
```



#### 类型判断instanceof

```java
// 类型判断
        if (a instanceof Cat)  {  // 猫做的事情 
            Cat c = (Cat)a;  
            c.work();  
        } else if (a instanceof Dog) { // 狗做的事情 
            Dog c = (Dog)a;  
            c.work();  
        }  
```

### 6.面向接口编程

面向接口编程是指在面向对向系统中所有的类或模块之间的交互由接口来完成。面向接口编程大大的降低了类之间的耦合度提高程序的扩展性。接口和实现分离了，适于团队的协作开发。 接口本质上就是由制定者来协调实现者和调用者之间的关系。 只有实现者和调用者都遵循“面向接口编程”这个准则，制定者的协调目的才能达到。 

* 在项目中的意义：接口在项目就是一个业务逻辑，面向接口编程就是先把客户的业务提取出来，作为接口。业务具体实现通过该接口的实现类来完成。当客户需求变化时，只需编写该业务逻辑的新的实现类，通过更改配置文件(例如Spring框架)中该接口的实现类就可以完成需求，不需要改写现有代码，减少对系统的影响。 采用基于接口编程的项目，业务逻辑清晰，代码易懂，方便扩展，可维护性强。即使更换一批人员，新来的人依然可以快速上手。对于公司来说，意义更大。
* 在Java中的意义：Java本身也是一个不断完善的语言，他也在频繁的改动他的系统API来完善，他的API是一个庞大的体系，互相关联，如果不采用接口，而都是用实现类的话，那么API的改动就会给整个体系带来不稳定。而且如果改动API，那么就会有大量采用旧API的项目因无法正常运行，会损失大量客户。换句话说，JDK已经发布的API是一种承诺，一经发布就不能更改，即使原来API存在各种各样的问题（例如java.util.Properties类就是一个失败的例子）也必须保留，于是在Java里就出现了不建议使用的方法，但JDK依然提供该方法。而且Java语言本身是一个跨平台的语言，为了满足在各个平台下运行，就必须把各种操作做成接口，在编写各个平台下的实现类。
* 设计模式的体现：在设计模式的原则里的开闭原则，其实就是要使用接口来实现对扩展开放，对修改关闭。在设计模式的其他原则里也有关于基于接口编程的原则，即依赖倒转的设计原则(DIP)----高层模块不应该依赖于底层模块。二者都应该依赖于抽象；抽象不应该依赖于细节，细节应该依赖于抽象(注：来自《敏捷软件开发--原则、模式与实践》Robert C.Martin著)。在使用面向接口的编程过程中，将具体逻辑与实现分开，减少了各个类之间的相互依赖，当各个类变化时，不需要对已经编写的系统进行改动，添加新的实现类就可以了，不在担心新改动的类对系统的其他模块造成影响。 

优点： 

* 接口和实现分离了，适于团队的协作开发。 
* 主要为了实现松散耦合的系统，便于以后升级，扩展。

缺点： 

* 设计难了，在你没有写实现的时候，就得想好接口，接口一变，全部乱套，这就是所谓的设计比实现难。 


在设计程序时应当根据具体的分析来确定是使用抽象类还是接口。abstract类除了提供重要的需要重写的abstract方法外，也提供了子类可以继承的变量和非abstract方法。如果某个重要问题需要使用继承才能更好地解决，比如，子类需要重写父类的abstract方法，还需要从父类继承一些变量或继承一些重要的非abstract方法，就可以考虑用abstract类。如果某个问题不需要继承，只是需要若干个类给出某些重要的abstract方法的实现细节，就可以考虑使用接口。

## 九、代码块和执行顺序

根据其位置和声明的不同，可以分为：

- 普通代码块	

  1、普通代码块定义在方法体中
  2、普通代码块与构造代码块的格式一致都是`{}`
  3、普通代码块与构造代码块唯一能直接看出的区别是**构造代码块是在类中定义的，而普通代码块是在方法体中定义的**

  

- 构造代码块

  只要该类实例了一个对象，构造代码就执行一次，利用每次创建对象的时候都会提前调用一次构造代码块特性，所以它可以做统计创建对象的次数功能。

  1、构造代码块在创建对象时被调用，每次创建对象都会调用一次
  2、构造代码块优先于构造函数执行，同时构造代码块的运行依赖于构造函数
  3、构造代码块在类中定义

  

- 静态代码块

  Java静态代码块中的代码会在类加载JVM时运行，且只被执行一次，也就是说这些代码不需要实例化类就能够被调用。一般情况下,如果有些代码必须在项目启动的时候就执行的时候,就需要使用静态代码块，所以静态块常用来执行类属性的初始化！

  1、Java静态代码块中的代码会在类加载JVM时运行，且只被执行一次
  2、静态块常用来执行类属性的初始化
  3、静态块优先于各种代码块以及构造函数，如果一个类中有多个静态代码块，会按照书写顺序依次执行
  4、静态代码块可以定义在类的任何地方中除了方法体中【这里的方法体是任何方法体】
  5、静态代码块不能访问普通变量

  

```java
public class Animal {
        static {
            System.out.println("Animal静态代码块");
        }
        {
            System.out.println("Animal构造代码块");
        }
        public Animal(){
            System.out.println("Animal构造函数");
        }
        public void eat(){
            System.out.println("Animal普通代码块");
        }
}
```

执行顺序：**静态代码块 > 构造代码块 > 构造函数 > 普通代码块**

```java
public class Dog extends Animal{
    static {
        System.out.println("Dog静态代码块");
    }
    {
        System.out.println("Dog构造代码块");
    }
    public Dog(){
        System.out.println("Dog构造函数");
    }
    public void eat(){
        System.out.println("Dog普通代码块");
    }
}

```

在继承子类中执行行顺序为：**父类静态块——>子类静态块——>父类构造代码块——>父类构造函数——>子类构造代码块——>子类构造函数**

## 十、异常

异常就是有异于常态，和正常情况不一样，有错误出现。在java中，将程序执行过程中的不正常的情况称之为异常，开发过程中的语法错误和逻辑错误不是异常，发生异常时java会阻止当前方法或作用域的情况。

### 1.Throwable

**Throwable**是java中所有异常和错误的超类,其两个子类为 Error(错误) 和 Exception(异常)。

- **Error**： 是程序中无法处理的错误，表示运行应用程序中出现了严重的错误。此类错误一般表示代码运行时JVM出现问题。通常有VirtualMachineError（虚拟机运行错误）、NoClassDefFoundError（类定义错误）等。比如说当jvm耗完可用内存时，将出现OutOfMemoryError。此类错误发生时，JVM将终止线程。非代码性错误。因此，当此类错误发生时，应用不应该去处理此类错误。
- **Exception**： 是程序本身可以捕获并且可以处理的异常。其中可分为运行时异常（RuntimeException）和非运行时异常，也叫做受检异常。RuntimeException类极其子类表示JVM在运行期间可能出现的错误。编译器不会检查此类异常，并且不要求处理异常，比如用空值对象的引用（NullPointerException）、数组下标越界（ArrayIndexOutBoundException）。此类异常属于不可查异常，一般是由程序逻辑错误引起的，在程序中可以选择捕获处理，也可以不处理。 Exception中除RuntimeException极其子类之外的异常。编译器会检查此类异常，如果程序中出现此类异常，比如说IOException，必须对该异常进行处理，要么使用try-catch捕获，要么使用throws语句抛出，否则编译不通过。

![异常][java-exception]

### 2.异常捕获处理try-catch-finally

```java
try{
  //能出现异常的代码
}catch(NullPointerException e){//子类异常捕获放前面
  //处理异常的代码
}catch(Exception e){
  //处理异常的代码
}finally{
  //释放资源代码
}
```



- 将可能出现异常的代码放到try{}中, 运行时, 如果代码发成了异常的话,就会生成一个对应的异常类的对象.这个产生的异常对象会与catch的异常类型相匹配,匹配成功后就被 catch 捕获,然后运行catch{}中的代码, 一般catch中的代码为处理异常的代码, 比如返回异常的信息和返回异常的详细信息等. 一旦异常处理完成,就会跳出当前的try-catch结构无论有没有发生异常finally中的代码都会最后被执行

- catch多个异常类型的时候, 如果有子父类关系,小的范围写上面大的范围写下面; 如果没有子父类关系,谁在上谁在下无所谓.
- 常用的异常对象处理方式: ① e.getMessage() ② e.printSrackTrace()
- 在try结构中生命的变量，在出了try结构以后，就不能在被调用。如果想避免这种情况，就需要在try之前声明变量并初始化，在try中赋值。
- 如果finally里面有return那么返回的一定是finally里面的
- try-catch-finally结构可以相互嵌套

### 3.throw和throws

throw关键字可用来手动抛出异常，如：

```java
throw new RuntimeException();
```

throws关键是用来声明方法有可能抛出的异常，如：

```java
public void withdraw(double amount) throws RemoteException,InsufficientFundsException {
     // Method implementation
}
```



### 4.自定义异常封装

可通过实现Throwable或继承Exception/RuntimeException自定义异常。通常用来封装业务错误信息，并提供全局编码ID来管理应用的业务错误信息。

```java
public class MyException extends RuntimeException {

    private String errorCode;
    private String errorMsg;

    public MyException(String errorCode, String errorMsg) {
        super(errorMsg);
        this.errorCode = errorCode;
        this.errorMsg = errorMsg;
    }
}

```



### 5.try-with-resource

JDK7 之后，Java 新增的 **try-with-resource** 语法糖来打开资源，并且可以在语句执行完毕后确保每个资源都被自动关闭 。JDK7 之前所有被打开的系统资源，比如流、文件或者 Socket 连接等，都需要被开发者手动关闭，否则将会造成资源泄露。

```java
try (resource declaration) {
  // 使用的资源
} catch (Exception e1) {
  // 异常块
}
```

例子：

```java
import java.io.*;

public class RunoobTest {

    public static void main(String[] args) {
    String line;
        try(BufferedReader br = new BufferedReader(new FileReader("test.txt"))) {
            while ((line = br.readLine()) != null) {
                System.out.println("Line =>"+line);
            }
        } catch (IOException e) {
            System.out.println("IOException in try block =>" + e.getMessage());
        }
    }
}
```

try-with-resources 语句中可以声明多个资源，方法是使用分号 **;** 分隔各个资源：

```java
import java.io.*;
import java.util.*;
class RunoobTest {
    public static void main(String[] args) throws IOException{
        try (Scanner scanner = new Scanner(new File("testRead.txt")); 
            PrintWriter writer = new PrintWriter(new File("testWrite.txt"))) {
            while (scanner.hasNext()) {
                writer.print(scanner.nextLine());
            }
        }
    }
}
```



## 十一、内部类

Java 一个类中可以嵌套另外一个类，语法格式如下：

```java
class OuterClass {   // 外部类
    // ...
    class NestedClass { // 嵌套类，或称为内部类
        // ...
    }
}
```

内部类包括：非静态内部类、静态内部类、匿名内部类和局部内部类。

### 1.非静态内部类

非静态内部类是一个类中嵌套着另外一个类。 它有访问外部类成员的权限， 通常被称为内部类。由于内部类嵌套在外部类中，因此必须首先实例化外部类，然后创建内部类的对象来实现。成员内部类可以无条件访问外部类的所有成员属性和成员方法（包括private成员和静态成员）。同样，外部类也可以访问内部类的所有成员变量和方法（包括private），但外部类想访问成员内部类的成员，必须先创建一个成员内部类的对象，再通过指向这个对象的引用来访问。内部类可以使用 private 或 protected 来修饰，如果你不希望内部类被外部类访问可以使用 private 修饰符。

```java
class OuterClass {
  int x = 10;

  class InnerClass {
    int y = 5;
  }
}

public class MyMainClass {
  public static void main(String[] args) {
    OuterClass myOuter = new OuterClass();
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
    System.out.println(myInner.y + myOuter.x);
  }
}
```

在api接口响应数据中，我们可以使用成员内部类这种方式来定义复杂的结构，实现json序列化：

```java
@Data
@EqualsAndHashCode
public class PaoPaoMallCrowdActivityInfoResponse {
	private String code;
    private String msg;
    private PaoPaoMallCrowdActivityInfoResponseData data;
    public boolean isSuccess() {
        return "A00000".equals(code) && data!=null;
    }
    
    @Data
    public class PaoPaoMallCrowdActivityInfoResponseData {
    	private long activityId;
    	private int orderNum;
    	private int targetNum;
    	private long startTime;
    	private long endTime;
    }
}

```



### 2.静态内部类

静态内部类可以使用 static 关键字定义，静态内部类我们不需要创建外部类来访问，可以直接访问它。

```java
class OuterClass {
  int x = 10;

  static class InnerClass {
    int y = 5;
  }
}

public class MyMainClass {
  public static void main(String[] args) {
    OuterClass.InnerClass myInner = new OuterClass.InnerClass();
    System.out.println(myInner.y);
  }
}
```

**注意：**静态内部类无法访问外部类的成员。

### 3.匿名内部类

匿名内部类是唯一一种没有构造器的类。正因为其没有构造器，所以匿名内部类的使用范围非常有限，大部分匿名内部类用于接口回调。匿名内部类在编译的时候由系统自动起名为Outter$1.class。一般来说，匿名内部类用于继承其他类或是实现接口，并不需要增加额外的方法，只是对继承方法的实现或是重写。

```java
public class Demo {
    private Runnable runnable = new Runnable() {
        @override
        public void run() {}
    }
}

```



### 4.局部内部类

局部内部类是定义在一个方法或者一个作用域里面的类，它和成员内部类的区别在于局部内部类的访问仅限于方法内或者该作用域内。局部内部类就像是方法里面的一个局部变量一样，是不能有public、protected、private以及static修饰符的。

```java
 
	public void test() {
		class InnerClass {
			private String name;
			final static String test = "1";
			public InnerClass(String name) {
				super();
				this.name = name;
			}
			public void say(String str) {
				System.out.println(name+":"+str);
			}
		}
		new InnerClass("test").say("hello");
	}

```



## 十二、泛型

Java 泛型（generics）是 JDK 5 中引入的一个新特性, 泛型提供了编译时类型安全检测机制，该机制允许程序员在编译时检测到非法的类型。泛型的本质是参数化类型，也就是说所操作的数据类型被指定为一个参数。泛型的好处是在编译的时候检查类型安全，并且所有的强制转换都是自动和隐式的，提高代码的重用率。泛型的一个附带好处是，消除源代码中的许多强制类型转换，这使得代码更加可读，并且减少了出错机会。

### 1.泛型方法

**泛型方法的规则：**

- 所有泛型方法声明都有一个类型参数声明部分（由尖括号分隔），该类型参数声明部分在方法返回类型之前。
- 每一个类型参数声明部分包含一个或多个类型参数，参数间用逗号隔开。一个泛型参数，也被称为一个类型变量，是用于指定一个泛型类型名称的标识符。
- 类型参数能被用来声明返回值类型，并且能作为泛型方法得到的实际参数类型的占位符。
- 泛型方法体的声明和其他方法一样。注意类型参数只能代表引用型类型，不能是原始类型（像 **int、double、char** 等）。

**java 中泛型标记符：**

- **E** - Element (在集合中使用，因为集合中存放的是元素)
- **T** - Type（Java 类）
- **K** - Key（键）
- **V** - Value（值）
- **N** - Number（数值类型）
- **？** - 表示不确定的 java 类型(类型通配符)

```java
public class GenericMethodTest
{
   // 泛型方法 printArray                         
   public static < E > void printArray( E[] inputArray )
   {
      // 输出数组元素            
         for ( E element : inputArray ){        
            System.out.printf( "%s ", element );
         }
         System.out.println();
    }
 
    public static void main( String args[] )
    {
        // 创建不同类型数组： Integer, Double 和 Character
        Integer[] intArray = { 1, 2, 3, 4, 5 };
        Double[] doubleArray = { 1.1, 2.2, 3.3, 4.4 };
        Character[] charArray = { 'H', 'E', 'L', 'L', 'O' };
 
        System.out.println( "整型数组元素为:" );
        printArray( intArray  ); // 传递一个整型数组
 
        System.out.println( "\n双精度型数组元素为:" );
        printArray( doubleArray ); // 传递一个双精度型数组
 
        System.out.println( "\n字符型数组元素为:" );
        printArray( charArray ); // 传递一个字符型数组
    } 
}
```



### 2.泛型类

泛型类的声明和非泛型类的声明类似，除了在类名后面添加了类型参数声明部分。和泛型方法一样，泛型类的类型参数声明部分也包含一个或多个类型参数，参数间用逗号隔开。一个泛型参数，也被称为一个类型变量，是用于指定一个泛型类型名称的标识符。因为他们接受一个或多个参数，这些类被称为参数化的类或参数化的类型。

```java
public class Box<T> {
   
  private T t;
 
  public void add(T t) {
    this.t = t;
  }
 
  public T get() {
    return t;
  }
 
  public static void main(String[] args) {
    Box<Integer> integerBox = new Box<Integer>();
    Box<String> stringBox = new Box<String>();
 
    integerBox.add(new Integer(10));
    stringBox.add(new String("菜鸟教程"));
 
    System.out.printf("整型值为 :%d\n\n", integerBox.get());
    System.out.printf("字符串为 :%s\n", stringBox.get());
  }
}
```



## 十三、Class类和Object类

### 1.Class类

 Java程序在运行时，Java运行时系统一直对所有的对象进行所谓的运行时类型标识，即所谓的RTTI。这项信息纪录了每个对象所属的类。虚拟机通常使用运行时类型信息选准正确方法去执行，用来保存这些类型信息的类是Class类。Class类封装一个对象和接口运行时的状态，当装载类时，Class类型的对象自动创建。比如你创建一个***shapes***类，那么，JVM会生成一个内容是***shapes***的Class类的对象。Class类的作用是运行时提供或获得某个对象的类型信息，这些信息也可用于反射。

* **获取Class对象**

  ```java
  //方法1 forName
  public class shapes{}  
  Class obj= Class.forName("shapes");
  ```

  ```java
  //方法2 getClass()
  public class shapes{}
  shapes s1=new shapes();
  Class obj=s1.getClass();
  Class obj1=s1.getSuperclass();//这个函数作用是获取shapes类的父类的类型
  ```

  ```java
  //方法3 类字面量
  Class obj=String.class;
  Class obj1=int.class;
  ```

  

* **使用Class类的对象来生成目标类的实例**

  获取一个Class类的对象后，可以用 **newInstance()** 函数来生成目标类的一个实例。然而，该函数并不能直接生成目标类的实例，只能生成object类的实例。

  ```java
  Class obj=Class.forName("shapes");
  Object ShapesInstance=obj.newInstance();
  ```

  ```java
  //使用泛化Class引用生成带类型的目标实例
  Class<shapes> obj=shapes.class;
  shapes newShape=obj.newInstance();
  ```

**Class类方法：**

| 方法名             | 说明                                                         |
| :----------------- | :----------------------------------------------------------- |
| forName()          | (1)获取Class对象的一个引用，但引用的类还没有加载(该类的第一个对象没有生成)就加载了这个类。 (2)为了产生Class引用，forName()立即就进行了初始化。 |
| Object-getClass()  | 获取Class对象的一个引用，返回表示该对象的实际类型的Class引用。 |
| getName()          | 取全限定的类名(包括包名)，即类的完整名字。                   |
| getSimpleName()    | 获取类名(不包括包名)                                         |
| getCanonicalName() | 获取全限定的类名(包括包名)                                   |
| isInterface()      | 判断Class对象是否是表示一个接口                              |
| getInterfaces()    | 返回Class对象数组，表示Class对象所引用的类所实现的所有接口。 |
| getSupercalss()    | 返回Class对象，表示Class对象所引用的类所继承的直接基类。应用该方法可在运行时发现一个对象完整的继承结构。 |
| newInstance()      | 返回一个Oject对象，是实现“虚拟构造器”的一种途径。**使用该方法创建的类，必须带有无参的构造器**。 |
| getFields()        | 获得某个类的所有的公共（public）的字段，包括继承自父类的所有公共字段。 类似的还有getMethods和getConstructors。 |
| getDeclaredFields  | 获得某个类的自己声明的字段，即包括public、private和proteced，默认但是不包括父类声明的任何字段。类似的还有getDeclaredMethods和getDeclaredConstructors。 |

### 2.Object类

Java Object 类是所有类的父类，也就是说 Java 的所有类都继承了 Object，**子类可以使用 Object 的所有方法**。

**Object类的方法**：

* protected Object clone() 

  创建并返回一个对象的拷贝

* boolean equals(Object obj)

  比较两个对象是否相等

* protected void finalize()

  当 GC (垃圾回收器)确定不存在对该对象的有更多引用时，由对象的垃圾回收器调用此方法。

* Class getClass()

  获取对象的运行时对象的类

* int hashCode()

  获取对象的 hash 值

* void notify()

  唤醒在该对象上等待的某个线程

* void notifyAll()

  唤醒在该对象上等待的所有线程

* String toString()

  返回对象的字符串表示形式

* void wait()

  让当前线程进入等待状态。直到其他线程调用此对象的 notify() 方法或 notifyAll() 方法。

* void wait(long timeout)

  让当前线程处于等待(阻塞)状态，直到其他线程调用此对象的 notify() 方法或 notifyAll() 方法，或者超过参数设置的timeout超时时间。

* void wait(long timeout, int nanos)

  与 wait(long timeout) 方法类似，多了一个 nanos 参数，这个参数表示额外时间（以纳秒为单位，范围是 0-999999）。 所以超时的时间还需要加上 nanos 纳秒。。



## 十四、反射

反射是java语言的一个特性，它允程序在运行时（注意不是编译的时候）进行自我检查并且对内部的成员进行操作。反射是在运行状态中，对于任意一个类，都能够知道这个类的所有属性和方法,对于任意一个对象，都能够调用它的任意方法和属性,这种动态获取信息以及动态调用对象方法的功能称为java语言的反射机制。

**反射的具体实现：**

通过 Class 类获取成员变量、成员方法、接口、超类、构造方法等:

* getName()：获得类的完整名字。
* getFields()：获得类的public类型的属性。
* getDeclaredFields()：获得类的所有属性。包括private 声明的和继承类
* getMethods()：获得类的public类型的方法。
* getDeclaredMethods()：获得类的所有方法。包括private 声明的和继承类
* getMethod(String name, Class[] parameterTypes)：获得类的特定方法，name参数指定方法的名字，parameterTypes 参数指定方法的参数类型。
* getConstructors()：获得类的public类型的构造方法。
* getConstructor(Class[] parameterTypes)：获得类的特定构造方法，parameterTypes 参数指定构造方法的参数类型。
* newInstance()：通过类的不带参数的构造方法创建这个类的一个对象。

获取constructor：

```java
     try {
            Class clazz = Person.class;
            Constructor<Person> constructor1 = clazz.getConstructor();
            Constructor<Person> constructor2 = clazz.getConstructor(String.class, int.class, int.class, int.class, String.class);
            Person person1 = constructor1.newInstance();
            Person person2 = constructor2.newInstance("male", 33, 162, 60, "Sean");
        } catch (Exception e) {
            e.printStackTrace();
        }
```

获取field:

```java
        try {
            Class clazz = Person.class;
            Field[] fields = clazz.getDeclaredFields();
            for(Field field : fields){
                System.out.println(field.getName());
            }
            Field nameField = clazz.getDeclaredField("name");
            nameField.setAccessible(true);
            Person person = (Person)clazz.newInstance();
            nameField.set(person,"sean");
            Object name = nameField.get(person);
            System.out.println("name:"+name);

        }catch(Exception e){
            e.printStackTrace();
        }
```

获取method并执行：

```java
        try {
            Class clazz = Person.class;
            Method[] methods = clazz.getDeclaredMethods();
            for(Method method : methods){
                System.out.println(method.getName());
            }
            Method setName = clazz.getMethod("setName",String.class);
            Person person = (Person)clazz.newInstance();
            setName.invoke(person,"Sean");
            System.out.println("name:"+person.getName());

        }catch(Exception e){
            e.printStackTrace();
        }
```




## 十五、JavaIO与文件操作

Java.io 包几乎包含了所有操作输入、输出需要的类。所有这些流类代表了输入源和输出目标。Java.io 包中的流支持很多种格式，比如：基本类型、对象、本地化字符集等等。一个流可以理解为一个数据的序列。输入流表示从一个源读取数据，输出流表示向一个目标写数据。Java 为 I/O 提供了强大的而灵活的支持，使其更广泛地应用到文件传输和网络编程中。File、RandomAccessFile、InputStream、OutputStream、Reader和Writer是IO流的基本类。

### 1.文件操作

* **File类**

  File类是java.io提供对文件系统中文件以及文件夹进行操作的对象。File类保存文件或目录的各种数据信息，包括文件名、文件长度、最后修改时间、是否可读、获取当前文件的路径名、判断文件是否存在、获取当前目录中的文件列表、创建、删除文件和目录等方法。

* **RandomAccessFile类**

  该类支持读取和写入随机访问文件。随机读写文件的行为类似于存储在文件系统中的大型字节数组。隐含数组中有一种游标或索引，称为文件指针;输入操作从文件指针开始读取字节，并将文件指针前进到读取的字节数之后。如果随机访问文件是在读/写模式下创建的，则写入操作也可用;写入操作从文件指针开始写入字节，并将文件指针前进到写入的字节数以上。写入操作到达数组的末尾，数组会自动扩展。文件指针可以由 getFilePointer 方法读取，并由 seek 方法设置。对于此类中的所有读取操作，如果到达文件末尾，则在读取所需的字节数之前，将抛出 EOFException（这是一种 IOException）。如果由于文件末尾以外的任何原因无法读取任何字节，则会抛出 EOFException 以外的 IOException。特别是，如果流已关闭，则可能会抛出 IOException。

### 2.IO流

流可以理解为一个数据的序列，流是一组有顺序的，有起点和终点的字节集合，是对数据传输的总称或抽象。IO流的本质是数据传输，并且流是单向的。IO流主要分为两大类，字节流和字符流。字节流可以处理任何类型的数据，如图片，视频等，字符流只能处理字符类型的数据。IO流继承关系如下：

![IO][java-iostream]



## 十六、网络编程

网络编程是指编写运行在多个设备（计算机）的程序，这些设备都通过网络连接起来。java.net 包中 J2SE 的 API 包含有类和接口，它们提供低层次的通信细节。java.net 包中提供了两种常见的网络协议的支持：

- **TCP**：TCP（英语：Transmission Control Protocol，传输控制协议） 是一种面向连接的、可靠的、基于字节流的传输层通信协议，TCP 层是位于 IP 层之上，应用层之下的中间层。TCP 保障了两个应用程序之间的可靠通信。通常用于互联网协议，被称 TCP / IP。
- **UDP**：UDP （英语：User Datagram Protocol，用户数据报协议），位于 OSI 模型的传输层。一个无连接的协议。提供了应用程序之间要发送数据的数据报。由于UDP缺乏可靠性且属于无连接协议，所以应用程序通常必须容许一些丢失、错误或重复的数据包。

### 1.Socket

Socket套接字使用TCP提供了两台计算机之间的通信机制。 客户端程序创建一个套接字，并尝试连接服务器的套接字。当连接建立时，服务器会创建一个 Socket 对象。客户端和服务器现在可以通过对 Socket 对象的写入和读取来进行通信。java.net.Socket 类代表一个套接字，并且 java.net.ServerSocket 类为服务器程序提供了一种来监听客户端，并与他们建立连接的机制。

以下步骤在两台计算机之间使用套接字建立TCP连接时会出现：

- 服务器实例化一个 ServerSocket 对象，表示通过服务器上的端口通信。
- 服务器调用 ServerSocket 类的 accept() 方法，该方法将一直等待，直到客户端连接到服务器上给定的端口。
- 服务器正在等待时，一个客户端实例化一个 Socket 对象，指定服务器名称和端口号来请求连接。
- Socket 类的构造函数试图将客户端连接到指定的服务器和端口号。如果通信被建立，则在客户端创建一个 Socket 对象能够与服务器进行通信。
- 在服务器端，accept() 方法返回服务器上一个新的 socket 引用，该 socket 连接到客户端的 socket。

**连接建立后，通过使用 I/O 流在进行通信**，每一个socket都有一个输出流和一个输入流，客户端的输出流连接到服务器端的输入流，而客户端的输入流连接到服务器端的输出流。TCP 是一个双向的通信协议，因此数据可以通过两个数据流在同一时间发送。

**socket通信在java中的具体实现：**

* **ServerSocket类**

  服务器应用程序通过使用 java.net.ServerSocket 类以获取一个端口,并且侦听客户端请求。

* **Socket类**

  java.net.Socket 类代表客户端和服务器都用来互相沟通的套接字。客户端要获取一个 Socket 对象通过实例化 ，而 服务器获得一个 Socket 对象则通过 accept() 方法的返回值。

* **InetAddress类**

  这个类表示互联网协议(IP)地址。

服务端例子：

```java
import java.net.*;
import java.io.*;
 
public class GreetingServer extends Thread
{
   private ServerSocket serverSocket;
   
   public GreetingServer(int port) throws IOException
   {
      serverSocket = new ServerSocket(port);
      serverSocket.setSoTimeout(10000);
   }
 
   public void run()
   {
      while(true)
      {
         try
         {
            System.out.println("等待远程连接，端口号为：" + serverSocket.getLocalPort() + "...");
            Socket server = serverSocket.accept();
            System.out.println("远程主机地址：" + server.getRemoteSocketAddress());
            DataInputStream in = new DataInputStream(server.getInputStream());
            System.out.println(in.readUTF());
            DataOutputStream out = new DataOutputStream(server.getOutputStream());
            out.writeUTF("谢谢连接我：" + server.getLocalSocketAddress() + "\nGoodbye!");
            server.close();
         }catch(SocketTimeoutException s)
         {
            System.out.println("Socket timed out!");
            break;
         }catch(IOException e)
         {
            e.printStackTrace();
            break;
         }
      }
   }
   public static void main(String [] args)
   {
      int port = Integer.parseInt(args[0]);
      try
      {
         Thread t = new GreetingServer(port);
         t.run();
      }catch(IOException e)
      {
         e.printStackTrace();
      }
   }
}
```

客户端例子：

```java
import java.net.*;
import java.io.*;
 
public class GreetingClient
{
   public static void main(String [] args)
   {
      String serverName = args[0];
      int port = Integer.parseInt(args[1]);
      try
      {
         System.out.println("连接到主机：" + serverName + " ，端口号：" + port);
         Socket client = new Socket(serverName, port);
         System.out.println("远程主机地址：" + client.getRemoteSocketAddress());
         OutputStream outToServer = client.getOutputStream();
         DataOutputStream out = new DataOutputStream(outToServer);
 
         out.writeUTF("Hello from " + client.getLocalSocketAddress());
         InputStream inFromServer = client.getInputStream();
         DataInputStream in = new DataInputStream(inFromServer);
         System.out.println("服务器响应： " + in.readUTF());
         client.close();
      }catch(IOException e)
      {
         e.printStackTrace();
      }
   }
}
```

### 2.URL处理

URL（Uniform Resource Locator）中文名为统一资源定位符，有时也被俗称为网页地址。表示为互联网上的资源，如网页或者 FTP 地址。

```java
//URL 可以分为如下几个部分，其中protocol(协议)可以是 HTTP、HTTPS、FTP 和 File
protocol://host:port/path?query#fragment
```

Java提供了java.net包来URL，主要类有：

* URL

  在java.net包中定义了URL类，该类用来处理有关URL的内容。

* URLConnections

  调用一个URL类对象的openConnection() 方法返回一个 java.net.URLConnection。

##  十七、BIO、NIO和AIO

### 1.IO流中的同步和异步、阻塞和非阻塞

* **同步和异步**

  同步和异步是针对应用程序和内核的交互而言的，同步指的是用户进程触发IO 操作并等待或者轮询的去查看IO 操作是否就绪，而异步是指用户进程触发IO 操作以后便开始做自己的事情，而当IO 操作已经完成的时候会得到IO 完成的通知。使用同步 IO 时，Java 自己处理IO 读写；使用异步IO 时，Java 将 IO 读写委托给OS （操作系统）处理，需要将数据缓冲区地址和大小传给OS，前提是OS 需要支持异步IO操作API。

* **阻塞和非阻塞**

  阻塞和非阻塞是针对于进程在访问数据的时候，根据IO操作的就绪状态来采取的不同方式，说白了是一种读取或者写入操作方法的实现方式，阻塞方式下读取或者写入函数将一直等待，而非阻塞方式下，读取或者写入方法会立即返回一个状态值。使用阻塞IO时，Java调用会一直阻塞到读写完成才返回；使用非阻塞IO时，如果不能读写Java调用会马上返回，当IO事件分发器通知可读写时再继续进行读写，不断循环直到读写完成；

### 2.BIO

Blocking IO： 同步阻塞的编程方式。

BIO编程方式通常是在JDK1.4版本之前常用的编程方式。编程实现过程为：首先在服务端启动一个ServerSocket来监听网络请求，客户端启动Socket发起网络请求，默认情况下ServerSocket会建立一个线程来处理此请求，如果服务端没有线程可用，客户端则会阻塞等待或遭到拒绝。且建立好的连接，在通讯过程中，是同步的。同步并阻塞，服务器实现模式为一个连接一个线程，即客户端有连接请求时服务器端就需要启动一个线程进行处理，如果这个连接不做任何事情会造成不必要的线程开销，当然可以通过线程池机制改善。

BIO方式适用于连接数目比较小且固定的架构，这种方式对服务器资源要求比较高，并发局限于应用中，JDK1.4以前的唯一选择，但程序直观简单易理解。

### 3.NIO

Unblocking IO（New IO）： 同步非阻塞的编程方式。

NIO本身是基于事件驱动思想来完成的，其主要想解决的是BIO的大并发问题，NIO基于Reactor，当socket有流可读或可写入socket时，操作系统会相应的通知引用程序进行处理，应用再将流读取到缓冲区或写入操作系统。也就是说，这个时候，已经不是一个连接就要对应一个处理线程了，而是有效的请求，对应一个线程，当连接没有数据时，是没有工作线程来处理的。NIO的最重要的地方是当一个连接创建后，不需要对应一个线程，这个连接会被注册到多路复用器上面，所以所有的连接只需要一个线程就可以搞定，当这个线程中的多路复用器进行轮询的时候，发现连接上有请求的话，才开启一个线程进行处理，也就是一个请求一个线程模式。在NIO的处理方式中，当一个请求来的话，开启线程进行处理，可能会等待后端应用的资源(JDBC连接等)，其实这个线程就被阻塞了，当并发上来的话，还是会有BIO一样的问题。

### 4.AIO

Asynchronous IO： 异步非阻塞的编程方式。

与NIO不同，当进行读写操作时，只须直接调用API的read或write方法即可。这两种方法均为异步的，对于读操作而言，当有流可读取时，操作系统会将可读的流传入read方法的缓冲区，并通知应用程序；对于写操作而言，当操作系统将write方法传递的流写入完毕时，操作系统主动通知应用程序。即可以理解为，read/write方法都是异步的，完成后会主动调用回调函数。在JDK1.7中，这部分内容被称作NIO.2，主要在java.nio.channels包下增加了下面四个异步通道：

* AsynchronousSocketChannel
* AsynchronousServerSocketChannel
* AsynchronousFileChannel
* AsynchronousDatagramChannel



## 十八、序列化与反序列化

Java 提供了一种对象序列化的机制，该机制中，一个对象可以被表示为一个字节序列，该字节序列包括该对象的数据、有关对象的类型的信息和存储在对象中数据的类型。将序列化对象写入文件之后，可以从文件中读取出来，并且对它进行反序列化，也就是说，对象的类型信息、对象的数据，还有对象中的数据类型可以用来在内存中新建对象。整个过程都是 Java 虚拟机（JVM）独立的，也就是说，在一个平台上序列化的对象可以在另一个完全不同的平台上反序列化该对象。类 ObjectInputStream 和 ObjectOutputStream 是高层次的数据流，它们包含反序列化和序列化对象的方法。

### 1.序列化

ObjectOutputStream 类用来序列化一个对象，当序列化一个对象到文件时， 按照 Java 的标准约定是给文件一个 .ser 扩展名。

一个类的对象要想序列化成功，必须满足两个条件：

* 该类必须实现 java.io.Serializable 接口。

* 该类的所有属性必须是可序列化的。如果有一个属性不是可序列化的，则该属性必须注明是短暂的。

```java
import java.io.*;
 
public class SerializeDemo
{
   public static void main(String [] args)
   {
      Employee e = new Employee();
      e.name = "Reyan Ali";
      e.address = "Phokka Kuan, Ambehta Peer";
      e.SSN = 11122333;
      e.number = 101;
      try
      {
         FileOutputStream fileOut =
         new FileOutputStream("/tmp/employee.ser");
         ObjectOutputStream out = new ObjectOutputStream(fileOut);
         out.writeObject(e);
         out.close();
         fileOut.close();
         System.out.printf("Serialized data is saved in /tmp/employee.ser");
      }catch(IOException i)
      {
          i.printStackTrace();
      }
   }
}
```



### 2.反序列化

ObjectInputStream 类包含**readObject()**反序列化一个对象的方法,该方法从流中取出下一个对象，并将对象反序列化。它的返回值为Object，因此，你需要将它转换成合适的数据类型。

```java
import java.io.*;
 
public class DeserializeDemo
{
   public static void main(String [] args)
   {
      Employee e = null;
      try
      {
         FileInputStream fileIn = new FileInputStream("/tmp/employee.ser");
         ObjectInputStream in = new ObjectInputStream(fileIn);
         e = (Employee) in.readObject();
         in.close();
         fileIn.close();
      }catch(IOException i)
      {
         i.printStackTrace();
         return;
      }catch(ClassNotFoundException c)
      {
         System.out.println("Employee class not found");
         c.printStackTrace();
         return;
      }
      System.out.println("Deserialized Employee...");
      System.out.println("Name: " + e.name);
      System.out.println("Address: " + e.address);
      System.out.println("SSN: " + e.SSN);
      System.out.println("Number: " + e.number);
    }
}
```



注意：readObject() 方法中的 try/catch代码块尝试捕获 ClassNotFoundException 异常。对于 JVM 可以反序列化对象，它必须是能够找到字节码的类。如果JVM在反序列化对象的过程中找不到该类，则抛出一个 ClassNotFoundException 异常。



## 十九、集合

Java 集合框架主要包括两种类型的容器，一种是集合（Collection），存储一个元素集合，另一种是图（Map），存储键/值对映射。Collection 接口又有 3 种子类型，List、Set 和 Queue，再下面是一些抽象类，最后是具体实现类，常用的有 ArrayList、LinkedList、HashSet、LinkedHashSet、HashMap、LinkedHashMap 等等。

### 1.Collection

从下图可以看出Collection分为List、Set和Queue三种类型。Queue主要是用于线程池阻塞队列，这里主要讨论List和Set。

![][java-collection]

#### List和Set的区别

- Set 接口实例存储的是无序的，不重复的数据。List 接口实例存储的是有序的，可以重复的元素。
- Set 检索效率低下，删除和插入效率高，插入和删除不会引起元素位置改变 **<实现类有HashSet,TreeSet>**。
- List 和数组类似，可以动态增长，根据实际存储的数据的长度自动增长 List 的长度。查找元素效率高，插入删除效率低，因为会引起其他元素位置改变 **<实现类有ArrayList,LinkedList,Vector>** 。

#### ArrayList

该类也是实现了List的接口，实现了可变大小的数组，随机访问和遍历元素时，提供更好的性能。该类也是非同步的,在多线程的情况下不要使用。ArrayList 增长当前长度的50%，插入删除效率低。

#### LinkedList

链表（Linked list）是一种常见的基础数据结构，是一种线性表，但是并不会按线性的顺序存储数据，而是在每一个节点里存到下一个节点的地址。该类实现了List接口，允许有null（空）元素。主要用于创建链表数据结构，该类没有同步方法，如果多个线程同时访问一个List，则必须自己实现访问同步，解决方法就是在创建List时候构造一个同步的List。与 ArrayList 相比，LinkedList 的增加和删除的操作效率更高，而查找和修改的操作效率较低。

**以下情况使用 ArrayList :**

- 频繁访问列表中的某一个元素。
- 只需要在列表末尾进行添加和删除元素操作。

**以下情况使用 LinkedList :**

- 你需要通过循环迭代来访问列表中的某些元素。
- 需要频繁的在列表开头、中间、末尾等位置进行添加和删除元素操作。

#### Vector

该类和ArrayList非常相似，但是该类是同步的，可以用在多线程的情况，该类允许设置默认的增长长度，默认扩容方式为原来的2倍。

#### Stack

栈是Vector的一个子类，它实现了一个标准的后进先出的栈。

#### HashSet

HashSet 基于 HashMap 来实现的。该类实现了Set接口，不允许出现重复元素，不保证集合中元素的顺序，允许包含值为null的元素，但最多只能一个。HashSet 不是线程安全的， 如果多个线程尝试同时修改 HashSet，则最终结果是不确定的。 

#### LinkedHashSet

具有可预知迭代顺序的 `Set` 接口的哈希表和链接列表实现。

#### TreeSet

该类实现了Set接口，可以实现排序等功能。

### 2.Map

Map 接口存储一组键值对象，提供key（键）到value（值）的映射。其中常用的Map实现有：HashMap、LinkedHashMap、TreeMap、HashTable和Properties。

![Map继续关系][java-map]

#### HashMap

HashMap 是一个散列表，它存储的内容是键值对(key-value)映射。HashMap 实现了 Map 接口，根据键的 HashCode 值存储数据，具有很快的访问速度，最多允许一条记录的键为 null，不支持线程同步。HashMap 是无序的，即不会记录插入的顺序。HashMap 的 key 与 value 类型可以相同也可以不同，可以是字符串（String）类型的 key 和 value，也可以是整型（Integer）的 key 和字符串（String）类型的 value。

#### LinkedHashMap

继承于HashMap，使用元素的自然顺序对元素进行排序.

#### TreeMap

继承了AbstractMap，并且使用一颗树。与HashMap相比，TreeMap是一个能比较元素大小的Map集合，会对传入的key进行了大小排序。其中，可以使用元素的自然顺序，也可以使用集合中自定义的比较器来进行排序。不同于HashMap的哈希映射，TreeMap底层实现了树形结构。

#### HashTable

Hashtable是原始的java.util的一部分， 是一个Dictionary具体的实现 。然而，Java 2 重构的Hashtable实现了Map接口，因此，Hashtable现在集成到了集合框架中。它和HashMap类很相似，但是它支持线程同步。像HashMap一样，Hashtable在哈希表中存储键/值对。当使用一个哈希表，要指定用作键的对象，以及要链接到该键的值。然后，该键经过哈希处理，所得到的散列码被用作存储在该表中值的索引。

#### Properties

Properties 继承于 Hashtable，表示一个持久的属性集，属性列表中每个键及其对应值都是一个字符串。Properties 类被许多 Java 类使用。例如，在获取环境变量时它就作为 System.getProperties() 方法的返回值。

### 3.迭代器

Java迭代器（Iterator）是 Java 集合框架中的一种机制，它提供了一种在不暴露集合内部实现的情况下遍历集合元素的方法。Java Iterator（迭代器）不是一个集合，它是一种用于访问集合的方法，可用于迭代 ArrayList和 HashSet 等集合。Iterator 是 Java 迭代器最简单的实现，ListIterator 是 Collection API 中的接口， 它扩展了 Iterator 接口。

![集合迭代器][java-collection-iterator]

```java
import java.util.ArrayList;
import java.util.Iterator;

public class RunoobTest {
    public static void main(String[] args) {

        // 创建集合
        ArrayList<String> sites = new ArrayList<String>();
        sites.add("Google");
        sites.add("Runoob");
        sites.add("Taobao");
        sites.add("Zhihu");

        // 获取迭代器
        Iterator<String> it = sites.iterator();

        // 输出集合中的所有元素
        while(it.hasNext()) {
            System.out.println(it.next());
        }
    }
}
```



## 二十、Java8新特性

Java8 新增了非常多的特性，主要讨论以下几个：

- **Lambda 表达式** − Lambda 允许把函数作为一个方法的参数（函数作为参数传递到方法中）。
- **方法引用** − 方法引用提供了非常有用的语法，可以直接引用已有Java类或对象（实例）的方法或构造器。与lambda联合使用，方法引用可以使语言的构造更紧凑简洁，减少冗余代码。
- **默认方法** − 默认方法就是一个在接口里面有了一个实现的方法。
- **新工具** − 新的编译工具，如：Nashorn引擎 jjs、 类依赖分析器jdeps。
- **Stream API** −新添加的Stream API（java.util.stream） 把真正的函数式编程风格引入到Java中。
- **Date Time API** − 加强对日期与时间的处理。
- **Optional 类** − Optional 类已经成为 Java 8 类库的一部分，用来解决空指针异常。
- **Nashorn, JavaScript 引擎** − Java 8提供了一个新的Nashorn javascript引擎，它允许我们在JVM上运行特定的javascript应用。

### 1.Lambda 表达式

Lambda 表达式，也可称为闭包，它是推动 Java 8 发布的最重要新特性。Lambda 允许把函数作为一个方法的参数（函数作为参数传递进方法中）。使用 Lambda 表达式可以使代码变的更加简洁紧凑。

```
(parameters) -> expression
或
(parameters) ->{ statements; }
```

以下是lambda表达式的重要特征:

- **可选类型声明：**不需要声明参数类型，编译器可以统一识别参数值。
- **可选的参数圆括号：**一个参数无需定义圆括号，但多个参数需要定义圆括号。
- **可选的大括号：**如果主体包含了一个语句，就不需要使用大括号。
- **可选的返回关键字：**如果主体只有一个表达式返回值则编译器会自动返回值，大括号需要指定表达式返回了一个数值。

```
// 1. 不需要参数,返回值为 5  
() -> 5  
  
// 2. 接收一个参数(数字类型),返回其2倍的值  
x -> 2 * x  
  
// 3. 接受2个参数(数字),并返回他们的差值  
(x, y) -> x – y  
  
// 4. 接收2个int型整数,返回他们的和  
(int x, int y) -> x + y  
  
// 5. 接受一个 string 对象,并在控制台打印,不返回任何值(看起来像是返回void)  
(String s) -> System.out.print(s)
```



### 2.函数式接口

函数式接口(Functional Interface)就是一个有且仅有一个抽象方法，但是可以有多个非抽象方法的接口。函数式接口可以被隐式转换为 lambda 表达式。

如定义了一个函数式接口如下：

```java
@FunctionalInterface
interface GreetingService 
{
    void sayMessage(String message);
}
```

那么就可以使用Lambda表达式来表示该接口的一个实现(注：JAVA 8 之前一般是用匿名类实现的)：

```java
GreetingService greetService1 = message -> System.out.println("Hello " + message);
```

java.util.function 它包含了很多类，用来支持 Java的 函数式编程，该包中的函数式接口有：

| 序号 | 接口 & 描述                                                  |
| :--- | :----------------------------------------------------------- |
| 1    | **BiConsumer<T,U>**代表了一个接受两个输入参数的操作，并且不返回任何结果 |
| 2    | **BiFunction<T,U,R>**代表了一个接受两个输入参数的方法，并且返回一个结果 |
| 3    | **BinaryOperator<T>**代表了一个作用于于两个同类型操作符的操作，并且返回了操作符同类型的结果 |
| 4    | **BiPredicate<T,U>**代表了一个两个参数的boolean值方法        |
| 5    | **BooleanSupplier**代表了boolean值结果的提供方               |
| 6    | **Consumer<T>**代表了接受一个输入参数并且无返回的操作        |
| 7    | **DoubleBinaryOperator**代表了作用于两个double值操作符的操作，并且返回了一个double值的结果。 |
| 8    | **DoubleConsumer**代表一个接受double值参数的操作，并且不返回结果。 |
| 9    | **DoubleFunction<R>**代表接受一个double值参数的方法，并且返回结果 |
| 10   | **DoublePredicate**代表一个拥有double值参数的boolean值方法   |
| 11   | **DoubleSupplier**代表一个double值结构的提供方               |
| 12   | **DoubleToIntFunction**接受一个double类型输入，返回一个int类型结果。 |
| 13   | **DoubleToLongFunction**接受一个double类型输入，返回一个long类型结果 |
| 14   | **DoubleUnaryOperator**接受一个参数同为类型double,返回值类型也为double 。 |
| 15   | **Function<T,R>**接受一个输入参数，返回一个结果。            |
| 16   | **IntBinaryOperator**接受两个参数同为类型int,返回值类型也为int 。 |
| 17   | **IntConsumer**接受一个int类型的输入参数，无返回值 。        |
| 18   | **IntFunction<R>**接受一个int类型输入参数，返回一个结果 。   |
| 19   | **IntPredicate**：接受一个int输入参数，返回一个布尔值的结果。 |
| 20   | **IntSupplier**无参数，返回一个int类型结果。                 |
| 21   | **IntToDoubleFunction**接受一个int类型输入，返回一个double类型结果 。 |
| 22   | **IntToLongFunction**接受一个int类型输入，返回一个long类型结果。 |
| 23   | **IntUnaryOperator**接受一个参数同为类型int,返回值类型也为int 。 |
| 24   | **LongBinaryOperator**接受两个参数同为类型long,返回值类型也为long。 |
| 25   | **LongConsumer**接受一个long类型的输入参数，无返回值。       |
| 26   | **LongFunction<R>**接受一个long类型输入参数，返回一个结果。  |
| 27   | **LongPredicate**R接受一个long输入参数，返回一个布尔值类型结果。 |
| 28   | **LongSupplier**无参数，返回一个结果long类型的值。           |
| 29   | **LongToDoubleFunction**接受一个long类型输入，返回一个double类型结果。 |
| 30   | **LongToIntFunction**接受一个long类型输入，返回一个int类型结果。 |
| 31   | **LongUnaryOperator**接受一个参数同为类型long,返回值类型也为long。 |
| 32   | **ObjDoubleConsumer<T>**接受一个object类型和一个double类型的输入参数，无返回值。 |
| 33   | **ObjIntConsumer<T>**接受一个object类型和一个int类型的输入参数，无返回值。 |
| 34   | **ObjLongConsumer<T>**接受一个object类型和一个long类型的输入参数，无返回值。 |
| 35   | **Predicate<T>**接受一个输入参数，返回一个布尔值结果。       |
| 36   | **Supplier<T>**无参数，返回一个结果。                        |
| 37   | **ToDoubleBiFunction<T,U>**接受两个输入参数，返回一个double类型结果 |
| 38   | **ToDoubleFunction<T>**接受一个输入参数，返回一个double类型结果 |
| 39   | **ToIntBiFunction<T,U>**接受两个输入参数，返回一个int类型结果。 |
| 40   | **ToIntFunction<T>**接受一个输入参数，返回一个int类型结果。  |
| 41   | **ToLongBiFunction<T,U>**接受两个输入参数，返回一个long类型结果。 |
| 42   | **ToLongFunction<T>**接受一个输入参数，返回一个long类型结果。 |
| 43   | **UnaryOperator<T>**接受一个参数为类型T,返回值类型也为T。    |



### 3.方法引用

方法引用通过方法的名字来指向一个方法。方法引用可以使语言的构造更紧凑简洁，减少冗余代码。方法引用使用一对冒号 **::** 。

- **构造器引用：**它的语法是Class::new，或者更一般的Class< T >::new实例如下：

  ```java
  final Car car = Car.create( Car::new ); final List< Car > cars = Arrays.asList( car );
  ```

  

- **静态方法引用：**它的语法是Class::static_method，实例如下：

  ```java
  cars.forEach( Car::collide );
  ```

  

- **特定类的任意对象的方法引用：**它的语法是Class::method实例如下：

  ```java
  cars.forEach( Car::repair );
  ```

  

- **特定对象的方法引用：**它的语法是instance::method实例如下：

  ```java
  final Car police = Car.create( Car::new ); cars.forEach( police::follow );
  ```

  

### 4.接口默认方法

Java 8 新增了接口的默认方法。简单说，默认方法就是接口可以有实现方法，而且不需要实现类去实现其方法。我们只需在方法名前面加个 default 关键字即可实现默认方法。

```java
public interface Vehicle {
   default void print(){
      System.out.println("我是一辆车!");
   }
}
```

调用接口的默认方法：

```java
Vehicle.super.print();
```



### 5.Stream API

Java 8 API添加了一个新的抽象称为流Stream，可以让你以一种声明的方式处理数据。Stream 使用一种类似用 SQL 语句从数据库查询数据的直观方式来提供一种对 Java 集合运算和表达的高阶抽象。Stream API可以极大提高Java程序员的生产力，让程序员写出高效率、干净、简洁的代码。这种风格将要处理的元素集合看作一种流， 流在管道中传输， 并且可以在管道的节点上进行处理， 比如筛选， 排序，聚合等。元素流在管道中经过中间操作（intermediate operation）的处理，最后由最终操作(terminal operation)得到前面处理的结果。

Stream（流）是一个来自数据源的元素队列并支持聚合操作

- **元素**是特定类型的对象，形成一个队列。 Java中的Stream并不会存储元素，而是按需计算。
- **数据源** 流的来源。 可以是集合，数组，I/O channel， 产生器generator 等。
- **聚合操作** 类似SQL语句一样的操作， 比如filter, map, reduce, find, match, sorted等。

和以前的Collection操作不同， Stream操作还有两个基础的特征：

- **Pipelining**: 中间操作都会返回流对象本身。 这样多个操作可以串联成一个管道， 如同流式风格（fluent style）。 这样做可以对操作进行优化， 比如延迟执行(laziness)和短路( short-circuiting)。
- **内部迭代**： 以前对集合遍历都是通过Iterator或者For-Each的方式, 显式的在集合外部进行迭代， 这叫做外部迭代。 Stream提供了内部迭代的方式， 通过访问者模式(Visitor)实现。

在 Java 8 中, 集合接口有两个方法来生成流：

- **stream()** − 为集合创建串行流。
- **parallelStream()** − 为集合创建并行流。

Stream流迭代器：

* forEach 

  Stream 提供了新的方法 'forEach' 来迭代流中的每个数据。

  ```java
  Random random = new Random();
  random.ints().limit(10).forEach(System.out::println);
  ```

  

* map

  map 方法用于映射每个元素到对应的结果

  ```java
  List<Integer> numbers = Arrays.asList(3, 2, 2, 3, 7, 3, 5);
  // 获取对应的平方数
  List<Integer> squaresList = numbers.stream().map( i -> i*i).distinct().collect(Collectors.toList());
  ```

  

* filter

  filter 方法用于通过设置的条件过滤出元素。

  ```java
  List<String>strings = Arrays.asList("abc", "", "bc", "efg", "abcd","", "jkl");
  // 获取空字符串的数量
  long count = strings.stream().filter(string -> string.isEmpty()).count();
  ```

  

* limit

  limit 方法用于获取指定数量的流。

  ```java
  Random random = new Random();
  random.ints().limit(10).forEach(System.out::println);
  ```

  

* sorted

  sorted 方法用于对流进行排序。

  ```java
  Random random = new Random();
  random.ints().limit(10).sorted().forEach(System.out::println);
  ```

  

**Collectors** 类实现了很多归约操作，例如将流转换成集合和聚合元素。Collectors 可用于返回列表或字符串：

```java
List<String>strings = Arrays.asList("abc", "", "bc", "efg", "abcd","", "jkl");
List<String> filtered = strings.stream().filter(string -> !string.isEmpty()).collect(Collectors.toList());
 
System.out.println("筛选列表: " + filtered);
String mergedString = strings.stream().filter(string -> !string.isEmpty()).collect(Collectors.joining(", "));
System.out.println("合并字符串: " + mergedString);
```

创建并行流有两种方法：

* 对流调用parallel()方法

  ```java
  lists.stream().parallel();
  ```

  

* 对Collection集合调用parallelStream()方法

  ```java
  lists.parallelStream();
  ```

  

另外，一些产生统计结果的收集器也非常有用。它们主要用于int、double、long等基本类型上，它们可以用来产生类似如下的统计结果。

```java
List<Integer> numbers = Arrays.asList(3, 2, 2, 3, 7, 3, 5);
 
IntSummaryStatistics stats = numbers.stream().mapToInt((x) -> x).summaryStatistics();
 
System.out.println("列表中最大的数 : " + stats.getMax());
System.out.println("列表中最小的数 : " + stats.getMin());
System.out.println("所有数之和 : " + stats.getSum());
System.out.println("平均数 : " + stats.getAverage());
```



### 6.Optional类

Optional 类是一个可以为null的容器对象。如果值存在则isPresent()方法会返回true，调用get()方法会返回该对象。Optional 是个容器：它可以保存类型T的值，或者仅仅保存null。Optional提供很多有用的方法，这样我们就不用显式进行空值检测。Optional 类的引入很好的解决空指针异常。

```java
import java.util.Optional;
 
public class Java8Tester {
   public static void main(String args[]){
   
      Java8Tester java8Tester = new Java8Tester();
      Integer value1 = null;
      Integer value2 = new Integer(10);
        
      // Optional.ofNullable - 允许传递为 null 参数
      Optional<Integer> a = Optional.ofNullable(value1);
        
      // Optional.of - 如果传递的参数是 null，抛出异常 NullPointerException
      Optional<Integer> b = Optional.of(value2);
      System.out.println(java8Tester.sum(a,b));
   }
    
   public Integer sum(Optional<Integer> a, Optional<Integer> b){
    
      // Optional.isPresent - 判断值是否存在
        
      System.out.println("第一个参数值存在: " + a.isPresent());
      System.out.println("第二个参数值存在: " + b.isPresent());
        
      // Optional.orElse - 如果值存在，返回它，否则返回默认值
      Integer value1 = a.orElse(new Integer(0));
        
      //Optional.get - 获取值，值需要存在
      Integer value2 = b.get();
      return value1 + value2;
   }
}
```



| 序号 | 方法 & 描述                                                  |
| :--- | :----------------------------------------------------------- |
| 1    | **static <T> Optional<T> empty()**返回空的 Optional 实例。   |
| 2    | **boolean equals(Object obj)**判断其他对象是否等于 Optional。 |
| 3    | **Optional<T> filter(Predicate<? super <T> predicate)**如果值存在，并且这个值匹配给定的 predicate，返回一个Optional用以描述这个值，否则返回一个空的Optional。 |
| 4    | **<U> Optional<U> flatMap(Function<? super T,Optional<U>> mapper)**如果值存在，返回基于Optional包含的映射方法的值，否则返回一个空的Optional |
| 5    | **T get()**如果在这个Optional中包含这个值，返回值，否则抛出异常：NoSuchElementException |
| 6    | **int hashCode()**返回存在值的哈希码，如果值不存在 返回 0。  |
| 7    | **void ifPresent(Consumer<? super T> consumer)**如果值存在则使用该值调用 consumer , 否则不做任何事情。 |
| 8    | **boolean isPresent()**如果值存在则方法会返回true，否则返回 false。 |
| 9    | **<U>Optional<U> map(Function<? super T,? extends U> mapper)**如果有值，则对其执行调用映射函数得到返回值。如果返回值不为 null，则创建包含映射返回值的Optional作为map方法返回值，否则返回空Optional。 |
| 10   | **static <T> Optional<T> of(T value)**返回一个指定非null值的Optional。 |
| 11   | **static <T> Optional<T> ofNullable(T value)**如果为非空，返回 Optional 描述的指定值，否则返回空的 Optional。 |
| 12   | **T orElse(T other)**如果存在该值，返回值， 否则返回 other。 |
| 13   | **T orElseGet(Supplier<? extends T> other)**如果存在该值，返回值， 否则触发 other，并返回 other 调用的结果。 |
| 14   | **<X extends Throwable> T orElseThrow(Supplier<? extends X> exceptionSupplier)**如果存在该值，返回包含的值，否则抛出由 Supplier 继承的异常 |
| 15   | **String toString()**返回一个Optional的非空字符串，用来调试  |





[java-string]:https://raw.githubusercontent.com/HolyPaPa99/Java/main/images/java-string.png
[java-string1]:https://raw.githubusercontent.com/HolyPaPa99/Java/main/images/java-string1.png
[java-extends]:https://raw.githubusercontent.com/HolyPaPa99/Java/main/images/java-extends.png
[java-duotai]:https://raw.githubusercontent.com/HolyPaPa99/Java/main/images/java-duotai.jpeg
[java-exception]:https://raw.githubusercontent.com/HolyPaPa99/Java/main/images/Java-Exception.jpg
[java-iostream]:https://raw.githubusercontent.com/HolyPaPa99/Java/main/images/java-iostream.png
[java-collection]:https://raw.githubusercontent.com/HolyPaPa99/Java/main/images/java-collection.jpg
[java-map]:https://raw.githubusercontent.com/HolyPaPa99/Java/main/images/java-map.jpg
[java-collection-iterator]:https://raw.githubusercontent.com/HolyPaPa99/Java/main/images/java-collection-iterator.jpeg





