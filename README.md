# jersey-json

An attempt to release a jersey-json 1.20 that relies on jersey 1.x jars but that uses Jackson 2 instead of the EOL jackson 1.

* Have dropped one class: [JSONWithPadding](https://github.com/javaee/jersey-1.x/blob/master/jersey-json/src/main/java/com/sun/jersey/api/json/JSONWithPadding.java) because Jackson 2 code seemed quite different. If this class is useful, I can look at trying to bring it back.
