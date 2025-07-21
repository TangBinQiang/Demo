---
# aside: false

outline: deep
---
# 🌟 Java 入门学习笔记（超级详细）

## 📘 一、Java 简介

> Java 是一种广泛使用的 **面向对象编程语言**，具有跨平台、安全性高等特点。

### ✅ Java 的主要特性：

* ☕ 跨平台：一次编写，到处运行（JVM 支持）
* 🔒 安全性高：沙箱机制、内存管理
* 🧩 面向对象：支持封装、继承、多态
* 🔄 多线程支持：原生线程库
* 📚 类库丰富：生态成熟，应用广泛


## 🎯 二、Java 的优点

* ✅ 结构清晰，维护方便
* 🔁 跨平台兼容性好
* 🚀 社区庞大，资料丰富
* ♻️ 自动垃圾回收机制（GC）
* 🔐 安全性强
* 🧵 内建多线程
* 🌐 应用领域广泛（企业开发、移动应用、游戏、大数据）

---

## 💻 三、第一个 Java 程序

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

📌 编译：`javac HelloWorld.java`
🚀 运行：`java HelloWorld`

⚠️ 注意事项：

* 区分大小写
* 文件名和类名一致
* 使用英文标点

---

## ✏️ 四、注释类型

| 类型   | 语法         | 用途          |
| ---- | ---------- | ----------- |
| 单行注释 | `//`       | 一行简单说明      |
| 多行注释 | `/* … */`  | 多行注释内容      |
| 文档注释 | `/** … */` | 可用于生成文档 API |

---

## 🧮 五、基本数据类型

| 类型        | 大小  | 默认值        | 示例                  |
| --------- | --- | ---------- | ------------------- |
| `byte`    | 8位  | `0`        | `byte b = 1;`       |
| `short`   | 16位 | `0`        | `short s = 2;`      |
| `int`     | 32位 | `0`        | `int i = 3;`        |
| `long`    | 64位 | `0L`       | `long l = 4L;`      |
| `float`   | 32位 | `0.0f`     | `float f = 5.0f;`   |
| `double`  | 64位 | `0.0d`     | `double d = 6.0;`   |
| `char`    | 16位 | `'\u0000'` | `char c = 'A';`     |
| `boolean` | 1位  | `false`    | `boolean b = true;` |

🧵 其他：`String` 是对象类型，使用非常广泛。

### 🔁 类型转换

* **自动类型提升**：小 → 大（如 int → long）
* **强制类型转换**：

  ```java
  double a = 3.14;
  int b = (int) a; // 精度丢失
  ```

---

## 🪙 六、变量使用

```java
int a = 10;
int b;
b = 20;
int c1 = 30, c2 = 40;
```

📌 Java 变量命名规则：

* 必须以字母、下划线 `_` 或 `$` 开头
* 不能使用 Java 关键字
* 建议使用 **小驼峰命名法**：`studentName`

---

## ➕ 七、运算符分类

### ✅ 算术运算符：

* `+ - * / % ++ --`

### ✅ 赋值运算符：

* `= += -= *= /= %=`

### ✅ 比较运算符：

* `== != > < >= <=`

### ✅ 逻辑运算符：

* `&& || !`

### ✅ 位运算符：

* `& | ^ ~ << >>`

### ✅ 三元运算符：

```java
int max = (a > b) ? a : b;
```

---

## 🔁 八、条件判断结构

```java
if (score >= 90) {
    System.out.println("优秀");
} else if (score >= 60) {
    System.out.println("及格");
} else {
    System.out.println("不及格");
}
```

✅ 也可以使用三元表达式：

```java
String result = (score >= 60) ? "及格" : "不及格";
```

---

## 🎚️ 九、switch 多分支选择

```java
int day = 3;
switch(day) {
    case 1: System.out.println("星期一"); break;
    case 2: System.out.println("星期二"); break;
    default: System.out.println("其他");
}
```

⚠️ switch 支持的类型：

* JDK 7 前：`byte`, `short`, `char`, `int`
* JDK 7 起：支持 `String`
* JDK 14 起：支持 `->` 简洁语法

---

## 🎣 十、输入输出 & 随机数

### 📥 Scanner 接收用户输入

```java
import java.util.Scanner;
Scanner sc = new Scanner(System.in);
int age = sc.nextInt();
String name = sc.next();
```

### 🎲 Random 生成随机数

```java
import java.util.Random;
Random r = new Random();
int num = r.nextInt(10); // 0-9
```

📌 范围设定：`r.nextInt(max - min + 1) + min`

---

## 🔁 十一、循环结构

### ✅ while 循环

```java
int i = 1;
while (i <= 5) {
    System.out.println(i);
    i++;
}
```

### ✅ do...while 循环

```java
int i = 1;
do {
    System.out.println(i);
    i++;
} while (i <= 5);
```

### ✅ for 循环

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

### 🔂 嵌套循环：九九乘法表

```java
for (int i = 1; i <= 9; i++) {
    for (int j = 1; j <= i; j++) {
        System.out.print(j + "*" + i + "=" + (i * j) + "\t");
    }
    System.out.println();
}
```

### 🚪 跳出循环：

* `break`：跳出整个循环
* `continue`：跳过当前循环
* `return`：结束整个方法

---

如果你希望继续学习 **数组、方法、类与对象、继承、多态、异常、集合、IO、线程** 等高级部分，我可以继续扩展这个笔记系列 💡

是否为你继续生成 **进阶部分的学习笔记**（含图标和结构）？
