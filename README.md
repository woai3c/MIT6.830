# [MIT6.830](http://db.lcs.mit.edu/6.830/)
暂时没时间，有时间再搞...

## 问题
### 1. ant: srcdir attribute must be non-empty
[stackoverflow-ant-srcdir-attribute-must-be-non-empty](https://stackoverflow.com/questions/49104089/ant-srcdir-attribute-must-be-non-empty)

### 2. 错误: 编码 GBK 的不可映射字符
主要是 `QueryPlanVisualizer.java` 文件中的代码有特殊符号：
```xml
static final String JOIN = "⨝";
static final String HASH_JOIN = "⨝(hash)";
```
把 `⨝` 替换成 `$` 就好了。

### 3. [javac] 警告: [options] 未与 -source 8 一起设置引导类路径
将 `build.xml` 文件中的 `<property name="sourceversion" value="1.8"/>` 1.8 改成你的 JDK 版本。

例如我的 JDK 版本是 `11.0.2`，那就将它改成 `<property name="sourceversion" value="11.0.2"/>`。

## 参考资料
* [ANT的安装和配置（windows）](http://www.cnitblog.com/intrl/archive/2009/04/11/56254.html)
* [simple-db-hw](https://github.com/MIT-DB-Class/simple-db-hw)
* [course-info-2018](https://github.com/MIT-DB-Class/course-info-2018)
