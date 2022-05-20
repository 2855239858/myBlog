# Hive SQL

### 1. Primitive types

- Types are associated with the columns in the tables. The following Primitive types are supported:
- Integers
  - TINYINT—1 byte integer
  - SMALLINT—2 byte integer
  - INT—4 byte integer
  - BIGINT—8 byte integer
- Boolean type
  - BOOLEAN—TRUE/FALSE
- Floating point numbers
  - FLOAT—single precision
  - DOUBLE—Double precision
- Fixed point numbers
  - DECIMAL—a fixed point value of user defined scale and precision
- String types
  - STRING—sequence of characters in a specified character set
  - VARCHAR—sequence of characters in a specified character set with a maximum length
  - CHAR—sequence of characters in a specified character set with a defined length
- Date and time types
  - TIMESTAMP — A date and time without a timezone ("LocalDateTime" semantics)
  - TIMESTAMP WITH LOCAL TIME ZONE — A point in time measured down to nanoseconds ("Instant" semantics)
  - DATE—a date
- Binary types
  - BINARY—a sequence of bytes

The Types are organized in the following hierarchy (where the parent is a super type of all the children instances):

![image-20220520143548535](C:\Users\user\Documents\GitHub\myBlog\source\_posts\BigData - Hive SQL\image-20220520143548535.png)

This type hierarchy defines how the types are implicitly converted in the query language. Implicit conversion is allowed for types from child to an ancestor. So when a query expression expects type1 and the data is of type2, type2 is implicitly converted to type1 if type1 is an ancestor of type2 in the type hierarchy. Note that the type hierarchy allows the implicit conversion of STRING to DOUBLE.