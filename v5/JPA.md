🌱 Basic Level

    What is JPA, and how is it different from Hibernate?
    Explain the main annotations used in JPA.
    What is the purpose of the @Entity annotation?
    How do you define a primary key using JPA?
    What is the difference between @Table and @Entity annotations?

🔥 Medium Level

    What are the different types of JPA relationships, and how are they implemented?
    How do you implement a one-to-many relationship using JPA?
    What is the EntityManager, and how does it work in Spring Data JPA?
    How do you handle transactions in JPA?
    What is the difference between findById and getOne in Spring Data JPA?

🚀 Advanced Level

    How can you write custom queries in Spring Data JPA?
    What is the Criteria API in JPA, and when would you use it?
    How do you handle batch processing in JPA?
    Explain @Inheritance in JPA. What strategies are available, and when would you use them?
    What is JPQL, and how does it differ from native SQL?

⚡ Challenging Level

    How do you optimize performance with JPA in high-traffic applications?
    🚀 Summary: JPA Performance Optimization Checklist
    Optimization	Key Benefit
    ✅ LAZY Fetching & JOIN FETCH	Prevents unnecessary data loading
    ✅ @EntityGraph	Solves N+1 query issue
    ✅ Pagination (Pageable)	Avoids loading huge datasets in memory
    ✅ Caching (@Cacheable, Second-Level Cache)	Reduces DB load for frequently accessed data
    ✅ Batch Inserts (hibernate.jdbc.batch_size)	Improves insert/update performance
    ✅ Read-Only Transactions	Avoids unnecessary dirty-checking
    ✅ Indexing & DTO Projections	Speeds up queries
    ✅ Connection Pooling (HikariCP)	Improves DB connection efficiency
    ✅ Statement Caching	Reduces query parsing overhead
    ✅ Read-Replica Database	Handles high read traffic

    Explain the difference between @ElementCollection and @OneToMany.

    How do you handle entity versioning and optimistic locking in JPA?
        2️⃣ How Does JPA Handle @Version?

        When JPA detects a versioned entity update:

            It adds WHERE version = ? to the update statement.
            If no rows are updated, it throws OptimisticLockException.

        ✅ Generated SQL for Update

        UPDATE product 
        SET price = ?, version = version + 1 
        WHERE id = ? AND version = ?;

        If no row matches the WHERE condition, it means another transaction has updated the entity, causing an optimistic lock failure.

    What are the potential pitfalls of the N+1 select problem, and how do you resolve it?
    How do you manage caching in Spring Data JPA?

🧠 Very Challenging Level

    How would you design a multi-tenant architecture using JPA and Spring Data JPA?
    What strategies can be used to handle large datasets with JPA without running into memory issues?
    Explain how to implement a dynamic query building mechanism in Spring Data JPA without using the @Query annotation.
    How do you handle complex transaction scenarios with multiple data sources in Spring Data JPA?
    What are the best practices to manage EntityManager in a microservices architecture?

---------- round 2
🌱 Basic Level

    What is JPA, and how does it integrate with Hibernate?
    Explain the role of @Entity, @Table, and @Id annotations in JPA.
    What is the difference between @Column and @Transient annotations?
    How do you map a Java class to a database table using JPA?
    What are the common data types supported by JPA annotations?
    How do you perform basic CRUD operations using Spring Data JPA?
    What is the use of the @GeneratedValue annotation?
    How do you configure a JPA data source in a Spring Boot application?

🔥 Medium Level

    What are the different fetch types in JPA (EAGER vs. LAZY), and when would you use each?
    Explain the difference between @OneToMany and @ManyToOne annotations.
    How do you handle bidirectional relationships in JPA?
    What is the purpose of @JoinColumn and @JoinTable annotations?
    How do you use @Query annotation to create custom queries in Spring Data JPA?
    What is the difference between JpaRepository, CrudRepository, and PagingAndSortingRepository?
    How do you use @Modifying and @Transactional annotations with custom update queries?
    How do you handle pagination and sorting in Spring Data JPA?

🚀 Advanced Level

    What is the Criteria API in JPA, and how do you use it for dynamic queries?
    How do you manage entity lifecycle callbacks using @PrePersist, @PostPersist, etc.?
    What is the difference between EntityManager.persist() and EntityManager.merge()?
    How do you implement soft deletes using JPA?
    What is the role of @MappedSuperclass, and how does it differ from @Inheritance?
    How do you handle composite primary keys in JPA using @EmbeddedId and @IdClass?
    What is the EntityGraph feature in JPA, and how does it help in optimizing queries?
    How do you implement auditing in JPA using @CreatedDate, @LastModifiedDate, and @EntityListeners?

⚡ Challenging Level

    How do you handle the N+1 select problem, and what are the strategies to avoid it?
    How do you implement caching in Spring Data JPA using @Cacheable and @CacheEvict?
    What are the different types of locking (Pessimistic vs. Optimistic) in JPA?
    How do you implement @Version annotation for optimistic locking, and when would you use it?
    How do you handle bulk updates and deletes in JPA without loading entities into memory?
    What is the @SecondaryTable annotation, and when would you use it?
    How do you use Specification in Spring Data JPA for complex queries?
    How do you handle transactions across multiple databases using Spring Data JPA?

🧠 Very Challenging Level

    How do you design and implement a multi-tenant architecture using JPA and Spring Data JPA?
    What are the best practices for handling large datasets with JPA to avoid memory issues?
    How do you implement a custom Repository using @NoRepositoryBean in Spring Data JPA?
    How would you optimize bulk data imports with JPA in a high-performance system?
    How do you handle dynamic query construction without @Query using Querydsl or Specifications?
    What are the pitfalls of CascadeType.ALL, and how do you avoid unintentional data loss?
    How would you implement a custom JPA dialect for a non-standard SQL database?
    How do you handle sharding and partitioning of data with JPA in a distributed system?
    What strategies do you use to handle complex, nested relationships in large domain models using JPA?
    How do you implement Event Listeners in JPA for handling entity state changes dynamically?

---------------- round 3
🌱 Basic Level

    What is the purpose of JPA, and how does it differ from JDBC?
    How do you configure JPA in a Spring Boot project?
    What is the difference between @Basic and @Column annotations?
    How do you specify column names and constraints using @Column annotation?
    What is the @Temporal annotation used for in JPA?
    How do you define default values for entity fields in JPA?
    How do you perform a simple findAll() operation using Spring Data JPA?
    What is the difference between save() and saveAndFlush() methods in JpaRepository?
    How do you use @Enumerated for enum fields in JPA?
    How do you handle null values in JPA queries?

🔥 Medium Level

    How do you implement a many-to-many relationship in JPA?
    What is the purpose of the @MappedSuperclass annotation?
    How do you handle cascading operations with JPA (CascadeType.ALL, CascadeType.MERGE, etc.)?
    How do you configure a named query using @NamedQuery annotation?
    How do you create and execute native SQL queries using @Query(nativeQuery = true) in Spring Data JPA?
    What is the @OrderBy annotation, and how does it differ from Sort in JpaRepository?
    How do you handle read-only entities using JPA?
    What is the @Embeddable annotation, and when would you use it?
    How do you handle unidirectional and bidirectional relationships in JPA?
    What is the difference between @OneToOne and @ManyToOne mappings?

🚀 Advanced Level

    How do you implement @Inheritance strategies like SINGLE_TABLE, JOINED, and TABLE_PER_CLASS?
    How do you handle multi-column unique constraints using @UniqueConstraint?
    What is the difference between EntityManager.clear() and EntityManager.detach()?
    How do you handle database sequences and identity generation using @GeneratedValue strategies?
    How do you manage transactions manually using EntityTransaction in JPA?
    What is the @SqlResultSetMapping annotation used for in JPA?
    How do you implement custom repositories in Spring Data JPA?
    What is EntityGraph, and how do you use it to optimize complex queries?
    How do you handle large IN queries efficiently in JPA?
    How do you implement @Converter to handle custom data types in JPA entities?

⚡ Challenging Level

    What are the differences between persistence context and session in JPA and Hibernate?
    How do you handle entity detachment and merging scenarios in JPA?
    How do you manage batch processing in JPA to improve performance?
    What are the different strategies for caching (First Level, Second Level, Query Cache) in JPA?
    How do you handle lazy loading exceptions in JPA with OpenEntityManagerInViewFilter?
    What is the role of @DiscriminatorColumn and @DiscriminatorValue in inheritance mapping?
    How do you handle custom ResultSetMapping with complex queries in JPA?
    What are @CollectionTable and @ElementCollection, and how do they differ from @OneToMany?
    How do you implement an efficient pagination strategy in Spring Data JPA with large datasets?
    How do you use Specification API for dynamic query generation in Spring Data JPA?

🧠 Very Challenging Level

    How do you design a system with multi-database support using JPA and Spring Data JPA?
    What are the best practices to avoid Memory Leaks in large-scale JPA applications?
    How do you handle distributed transactions using JTA (Java Transaction API) in JPA?
    How do you use Interceptor or EntityListener to handle entity auditing dynamically?
    How do you implement Custom Dialects for non-standard SQL databases in JPA?
    What are the pitfalls of using CascadeType.REMOVE in a complex domain model?
    How do you handle performance issues related to flush() and clear() in large transactions?
    How do you manage Hibernate Envers for advanced auditing requirements in a JPA application?
    How do you handle Sharding and Partitioning in JPA when dealing with large distributed databases?
    How do you implement Read-Write Splitting using JPA in a microservices architecture?

-------------- round 4 
🌱 Basic Level

    What is JPA, and how does it differ from Hibernate?
        Answer: JPA (Java Persistence API) is a specification that defines a standard way to manage relational data in Java applications. Hibernate is a popular implementation of this specification, providing additional features beyond the standard.

    What is the purpose of the @Entity annotation in JPA?
        Answer: The @Entity annotation marks a Java class as an entity, indicating that it should be mapped to a table in the database.

    How do you define a primary key in a JPA entity?
        Answer: A primary key is defined using the @Id annotation on a field, and you can specify the generation strategy with the @GeneratedValue annotation.

    What is the role of the EntityManager in JPA?
        Answer: The EntityManager interface provides methods to interact with the persistence context, including operations like persisting, removing, and finding entities.

    How do you perform basic CRUD operations using JPA?
        Answer: Basic CRUD operations can be performed using methods like persist(), merge(), remove(), and find() provided by the EntityManager.

🔥 Medium Level

    What are the different types of relationships in JPA, and how are they mapped?
        Answer: JPA supports relationships like One-to-One, One-to-Many, Many-to-One, and Many-to-Many, which are mapped using annotations such as @OneToOne, @OneToMany, @ManyToOne, and @ManyToMany.

    Explain the concept of cascading in JPA.
        Answer: Cascading allows operations to be propagated from a parent entity to its related entities. This is managed using the cascade attribute in relationship annotations, with types like PERSIST, MERGE, REMOVE, etc.

    What is the difference between fetch types EAGER and LAZY in JPA?
        Answer: EAGER fetching retrieves related entities immediately, while LAZY fetching delays the retrieval until the related entity is accessed.

    How do you handle transactions in JPA?
        Answer: Transactions in JPA can be managed programmatically using the EntityTransaction API or declaratively using the @Transactional annotation in frameworks like Spring.

    What is JPQL, and how does it differ from SQL?
        Answer: JPQL (Java Persistence Query Language) is an object-oriented query language defined by JPA, operating on entity objects rather than directly on database tables, unlike SQL.

🚀 Advanced Level

    How does the @Inheritance annotation work in JPA?
        Answer: The @Inheritance annotation is used to define inheritance strategies for entity classes, with strategies like SINGLE_TABLE, JOINED, and TABLE_PER_CLASS.

    What is the purpose of the EntityManagerFactory in JPA?
        Answer: The EntityManagerFactory is responsible for creating EntityManager instances and is typically designed to be thread-safe and shared across the application.

    Explain the use of the Criteria API in JPA.
        Answer: The Criteria API allows for the creation of type-safe, dynamic queries in a programmatic way, as an alternative to using JPQL.

    How do you implement optimistic locking in JPA?
        Answer: Optimistic locking is implemented using the @Version annotation, which maintains a version field to detect concurrent modifications.

    What are entity listeners in JPA, and how are they used?
        Answer: Entity listeners are classes or methods annotated to receive callbacks on entity lifecycle events, such as @PrePersist and @PostLoad.

⚡ Challenging Level

    How do you handle the N+1 select problem in JPA?
        Answer: The N+1 select problem can be mitigated by using fetch joins in JPQL or configuring proper fetching strategies to reduce the number of queries executed.

    What is the difference between merge() and update() in JPA?
        Answer: In JPA, merge() is used to synchronize the state of a detached entity with the persistence context, while update() is not a standard JPA method but is specific to certain implementations like Hibernate.

    How do you implement batch processing in JPA?
        Answer: Batch processing can be achieved by batching insert or update operations and periodically flushing and clearing the persistence context to manage memory usage.

    Explain the concept of secondary tables in JPA.
        Answer: Secondary tables allow an entity to map its fields to multiple tables using the @SecondaryTable annotation, enabling the splitting of entity attributes across different tables.

    How do you manage multiple persistence units in a JPA application?
        Answer: Managing multiple persistence units involves defining multiple persistence-unit elements in the persistence.xml file and creating corresponding EntityManagerFactory beans for each unit.

🧠 Very Challenging Level

    How would you design a multi-tenant application using JPA?
        Answer: Designing a multi-tenant application can involve strategies like schema-based, database-based, or discriminator-based multitenancy, each requiring specific configurations and considerations in JPA.

    What are the implications of using CascadeType.REMOVE in JPA relationships?
        Answer: Using CascadeType.REMOVE propagates the remove operation to associated entities, which can lead to the deletion of related data, so it must be used cautiously to prevent unintended data loss.

    How do you handle large data sets efficiently in JPA?
        Answer: Efficient handling of large data sets can