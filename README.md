# jersey-json

A version of jersey-json 1.x that relies on jersey 1.x jars but that uses Jackson 2 instead of the EOL jackson 1.

* Built with the latest release of jersey 1.x - 1.19.4
* About a dozen jersey-json classes have been changed to use Jackson 2 instead of Jackson 1
* A drop in replacement for `com.sun.jersey:jersey-json`
* v1.20 uses Jackson 2.13.0 to match version used by the then current trunk of Apache Hadoop
* It may be necessary to downgrade due to https://github.com/FasterXML/jackson-jaxrs-providers/issues/134, a change that likely affects Jersey 1.x because jersey-core 1.19 relies on jsr311-api jar (an old version of the JAX-RS support)
* [HADOOP-15983](https://issues.apache.org/jira/browse/HADOOP-15983) is the target of this work - this lib may not be a good fit for other use cases
* This lib is used in Hadoop since its v3.3.5 release (March 2023).
* Have dropped one class: [JSONWithPadding](https://github.com/javaee/jersey-1.x/blob/master/jersey-json/src/main/java/com/sun/jersey/api/json/JSONWithPadding.java) - because Jackson 2 code seemed quite different. If this class is useful, I can look at trying to bring it back.
* Do not use with Jackson 2.15+ unless you are happy with the new StreamReadConstraints defaults that were introduced in [v2.15.0](https://github.com/FasterXML/jackson/wiki/Jackson-Release-2.15)

```
  <dependency>
    <groupId>com.github.pjfanning</groupId>
    <artifactId>jersey-json</artifactId>
    <version>1.20</version>
  </dependency>
```
