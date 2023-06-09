# spring-boot-rest-api-crud-mysql
Spring Boot Rest APIs with CRUD for MySQL. 

Each branch implements different features:

- ***basic_crud***: the JPA methods to implement the CRUD have been developed by means of the EntityManager. There is no security implemented.
- ***crud_spring_data_jpa***: The JPA methods for CRUD operations have been obtained by extending the JpaRepository. There is no security implemented.
- ***in_memory_spring_security***: provides CRUD APIs with basic in memory authentication and authorization with Spring Security.
- ***spring_security_jdbc_auth_default_tables***: provides CRUD APIs with Spring Security authentication via JDBC with default table (default Spring tbale names and columns-  cannot be changed) both with plaintext and bcrypt passwords (the code is the same the only thing that changes is the prefix {noop} or {bcrypt} before the passwords stored inside the database)
- ***spring_security_jdbc_auth_custom_tables***: provides CRUD APIs with Spring Security authentication via JDBC with custom tables
- ***spring_security_custom_tables_with_JPA_hibernate***: provides CRUD APIs with Spring security authentication via JDBC using JPA and Hibernate (which means that User and Role are now entities)
- ***spring_security_user_registration*** I have added to the previous branch a REST API to allow the registration of a new user following [this example](https://github.com/Baeldung/spring-security-registration). I need to add more features to handle the users though.

In each branch the folder ***sql-scripts*** contains the SQL scripts to be run in MySQL.

NOTE: to make use of Spring dev tools on Intellij in Settings -> Build, Execution, Deployment check Build Project Automatically and in Advanced Settings check Allow auto-make to start even if developed application is currently running.
