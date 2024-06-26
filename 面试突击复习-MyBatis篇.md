## MyBatis的优缺点

- 优点：
  - 基于SQL语句编程，相当灵活，不会对应用程序或者数据库的现有设计造成任何影响，SQL写在XML里，解除SQL与程序代码的耦合，便于统一管理；提供XML标签，支持编写动态SQL语句，并可重用。
  - 与JDBC相比，减少了大量代码，消除了JDBC冗余代码，不需要手动开关连接。
  - 很好与各种数据库兼容，mybatis使用jdbc来连接数据库，只要jdbc支持的数据库mybatis都支持。
  - 能够与spring很好集成
  - 提供映射标签，支持对象与数据库的ORM字段关系映射；提供对象关系映射标签，支持对象关系组件维护。
- 缺点：
  - SQL语句的编写工作量较大，尤其当字段多、关联表多时，对开发人员编写SQL语句的功底有一定要求。
  - SQL语句依赖于数据库，导致数据库移植性差，不能随意更换数据库。

## MyBatis与Hibernate有哪些不同？



## #{}和${}有什么不同？

- #{}是预编译处理、是占位符。${}是字符串替换，是拼接符
- Mybatis在处理#{}时，会将sql中的#{}替换为?号，调用preparedStatement来赋值。
- #{}的变量替换是在DBMS中，变量替换后，#{}对应的变量自动加上单引号。
- ${}的变量替换是在DBMS之外，变量替换后，${}对应的变量不会加上单引号。
- 使用#{}可以有效防止SQL注入，提高系统安全性。
