### Java 异常处理

[TOC]

####  org.hibernate.LazyInitializationException:  

```java
	org.hibernate.LazyInitializationException: could not initialize proxy - no Session
	
	使用 SpringDataJpa 规范时修改时不能使用 getOne() 方法查询，只能使用 findOne() 方式
```

####  org.springframework.dao.InvalidDataAccessApiUsageException：

##### &nbsp;&nbsp;&nbsp;&nbsp;  1. 加 @Transactional 注解：

```java
	org.springframework.dao.InvalidDataAccessApiUsageException: Executing an update/delete query; nested exception is javax.persistence.TransactionRequiredException: Executing an update/delete query
	
	使用 SpringDataJpa 规范时，自己添加的修改/删除方法需要加上 @Transactional 注解
```

#####&nbsp;&nbsp;&nbsp;&nbsp;  2. 加 @Modifying 注解：

```java
	org.springframework.dao.InvalidDataAccessApiUsageException: org.hibernate.hql.internal.QueryExecutionRequestException: Not supported for DML operations
	
	使用 SpringDataJpa 规范时，自己添加的修改/删除方法需要加上 @Modifying 注解
```
