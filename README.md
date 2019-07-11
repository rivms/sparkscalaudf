# Sample Scala UDF

## Databricks Deployment

To register as a permanent function usable across sessions and languages:
- Upload to a DBFS location, use the jar file location when registering
- Register the function 

```
%sql
create function default.udf_str_len AS 'com.acme.ScalaUDF' USING JAR 'dbfs:/FileStore/jars/f09f2c08_74af_45aa_b786_dac180177d3f-uber_sparkscalaudf_1_0_SNAPSHOT-0b24f.jar'
```

- Test the function using SparkSQL
