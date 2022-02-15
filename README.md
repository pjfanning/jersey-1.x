# jersey-json

An attempt to release a jersey-json 1.20 that relies on jersey 1.x jars but that uses Jackson 2 instead of the EOL jackson 1.

* About a dozen jersey-json classes have been changed to use Jackson 2 instead of Jackson 1
* Uses Jackson 2.13.0 to match version used by current trunk of Apache Hadoop
* [HADOOP-15983](https://issues.apache.org/jira/browse/HADOOP-15983) is the target of this work - this lib may not be a good fit for other use cases
* Have dropped one class: [JSONWithPadding](https://github.com/javaee/jersey-1.x/blob/master/jersey-json/src/main/java/com/sun/jersey/api/json/JSONWithPadding.java) - because Jackson 2 code seemed quite different. If this class is useful, I can look at trying to bring it back.

```
  <dependency>
    <groupId>com.github.pjfanning</groupId>
    <artifactId>jersey-json</artifactId>
    <version>1.20-SNAPSHOT</version>
  </dependency>
```
