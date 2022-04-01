# **SQL Options in Spark**

PySpark provides two main options when it comes to using straight SQL. Spark SQL and SQL Transformer.

### **1) Spark SQL**

Spark TempView provides two functions that allow users to run **SQL** queries against a Spark Dataframe.

- **createOrReplaceTempView:** The lifetime of this temporary view is tied to the SparkSession that was used to create the dataset. It creates (or replaces if that view name already exists) a lazily evaluated "view" that you can then use like a hive table in Spark SQL. It does not persist to memory unless you cache the dataset that underpins the view.
- **createGlobalTempView:** The lifetime of this temporary view is tied to this Spark application. This feature is useful when you want to share data among different sessions and keep alive until your application ends.
  
A **Spark Session vs. Spark Application:**

**Spark application** can be used:
- for a single batch job;
- an interactive session with multiple jobs;
- a long-lived server continually satisfying requests;
- A Spark job can consist of more than just a single map and reduce;
- can constst of more than one Spark Session.
  
A **Spark Session** on the other hand:
- is an interaction between two or more entities;
- can be created without creating SparkConf, SparkContext or SQLContext, (they're encapsulated within the SparkSession which is new to Spark 2.0).

### **2) SQL Transformer**

You also have the option to use the SQL transformer option where you can write free-form SQL scripts as well.

# **SQL Options within regular PySpark calls**

1. The expr function in PySpark SQL Function library;
2. PySpark selectExpr function

We will go over all these in detail so buckel up!