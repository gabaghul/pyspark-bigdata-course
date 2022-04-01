## **Handling Missing Data in Pyspark**

In the real world, most datasets you work with will be incomplete, which means you will have missing data. You have 2 basic options for filling in missing data (you will personally have to make the decision for what is the right approach):

1. Drop the missing data points (including the possibility of the entire row);
2. Fill them in with some other value (like the average).

There are also twi different types of missing data to be aware of:

1. null values represents "no value" or "nothing", it's not even an empty string or zero. It can be used to represent that nothing useful exists.
2. NaN stands for "Not a Number", it's usually the result of a mathematical operation that doesn't make sense, e.g 0.0/0.0

Let's cover examples of each of these methods!