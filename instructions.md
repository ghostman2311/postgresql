# 24 Jan

## Foregin key constraints around insertion

1. If user id doesn't exist postgresql will throw an error.
   ![Alt text](image.png)
2. If the user id doesn't exist then we can set it to null
   ![Alt text](image-1.png)

## Foregin key constraints around deletion

1. Suppose a user is deleted and it's id is used as foreign key in another table then we do this
   ![Alt text](image-2.png)

# 25 Jan

## Testing deletion constraints

1. Setting the on delete cascade
   ![Alt text](image-3.png)

2. Now delete the user where id = 1
   ![Alt text](image-4.png)

## Setting foreign key to null on delete

1. On delete set the null
   ![Alt text](image-5.png)

# 29 Jan

## Queries with joins and aggregations

1. This is our new table structure
   ![Alt text](image-6.png)

2. Some intersting questions
   ![Alt text](image-7.png)

3. Joins and aggregation
   ![Alt text](image-8.png)

## Joining Data from Different Tables

1. Problem
   ![Alt text](image-9.png)

2. Problem
   ![Alt text](image-11.png)

3. Solution
   ![image](https://github.com/ghostman2311/postgresql/assets/78917858/86aa6161-ffc8-47e7-a8a2-4105fb2c346d)

# 30 Jan

## Alternate form of syntax

1. Notes on join
   ![Alt text](image-12.png)

## Missing Data in Joins

1. If we add a record in photo table with user_id as null
2. Then In the join new photo will be not included because it doesn't have corresponding user.
3. But This violates our query requirements

## Why Wasn't it included

1. Explanation is quite simple because we don't find a match that's why it is not included in the output.

# 31 Jan

## Four kind of joins

1. Inner join
   ![Alt text](image-13.png)
2. Left outer join
   ![Alt text](image-14.png)
3. Right outer join
   ![Alt text](image-15.png)
4. Full Join
   ![Alt text](image-16.png)

# 3 Feb

## Does order really matter

1. You can clearly see the difference
   ![alt text](image-17.png)

## Where with join

1. Task
   ![alt text](image-18.png)

# 4 Feb

## Three way join

1. Find username, url and comment where user commented on his own photo.

# 5 Feb

## Picturing group by

1. Groupby and aggregation difference
   ![alt text](image-19.png)

2. Here is pictorial representation of groupby
   ![alt text](image-20.png)

3. You can visualize like this
   ![alt text](image-21.png)

4. To select a column in group by query then that colum must be present in group by or aggregate function.

## Aggregate function

1. Here are some examples
   ![alt text](image-22.png)

# 6 Feb

## Combining Group by with aggregates

1. We combine group by with aggregates like this
   ![alt text](image-23.png)

2. You can use this to visualise the internal working of group by
   ![alt text](image-24.png)
3. Null values are not counted in COUNT function
4. To count the all rows including some column has null we can do like this
   ![alt text](image-25.png)

## Visualizing more grouping

1. Here is a problem
   ![alt text](image-26.png)

2. Do all the excercises

- https://www.udemy.com/course/sql-and-postgresql/learn/quiz/4987192#notes

# 7 Feb

## Filtering groups with having

1. Order of important keywords
   ![alt text](image-27.png)
2. Having is only used with group by
3. Problem
   ![alt text](image-28.png)

4. Problem
   ![alt text](image-29.png)

5. Excercise on udemy

# 10 Feb

## Investigating the data set

1. Data now will be related to ecommerce data
   ![alt text](image-30.png)
2. Perform all the excercise

# 12 Feb

## The basics of sorting

1. By default if we order by some value then we go in ascending order
   ![alt text](image-31.png)

2. We can add DESC if we want in desc order

## Two Variations on sorting

1. If price are same for two column we can mention second criteria for sorting that is weight in our case
   ![alt text](image-32.png)

## Offset and limit

1. limit and offset
   ![alt text](image-33.png)

2. Offset example, It just means skip some number of rows from result set.
   ![alt text](image-34.png)

3. Limit example
   ![alt text](image-35.png)

4. Offset with limit example, In this example we are finding the most expensive products except the most expensive one.
   ![alt text](image-36.png)

# 13 Feb

## Handling sets with union

1. Problem
   ![alt text](image-37.png)

## A few notes on union

1. There should be one common column name with same datatype. If both the table has different column name then we can not use union

## Commanalities with intersect

1. Here is diagram for various operations
   ![alt text](image-38.png)

2. Problem: Find the common rows from both the table in previous problem.

## Removing commanalities with except

1. Notes
   ![alt text](image-39.png)

# 14 Feb

## What is subquery

1. Problem
   ![alt text](image-40.png)

# 15 Feb

## Thinking about structure of data

1. Subqueries can be used as
   ![alt text](image-41.png)

# 16 Feb

## Subqueries in select

1. Query must return a single value
2. Here is an example
   ![alt text](image-42.png)

# 18 Feb

## Subqueries in from

1. Continue again

# 22 Feb

## Subqueries in from

1. Initial query
   ![alt text](image-43.png)

2. Subquery in from must have an alias.
3. Basic rule with subqueries in from
   ![alt text](image-44.png)
4. Write the query yourself in above image.

# 6 March

## From subqueries that return a value

1. Final query
   ![alt text](image-45.png)

# 9 March

## Example of sub query in a from

1. Problem
   ![alt text](image-46.png)

2. First use group by to return the each user and their # of order

3. Final result
   ![alt text](image-47.png)

# 14 march

## Subquery in join clause

1. Theory
   ![alt text](image-48.png)

2. Final sol
   ![alt text](image-49.png)

# 15 March

## Subquery with where

1. Initial problem
   ![alt text](image-50.png)

# 16 March

## Data structure with where subqueries

1. Table
   ![alt text](image-51.png)

2. Query
   ![alt text](image-52.png)

# 17 March

## The not in operator with a list

1. Query
   ![alt text](image-53.png)

2. Solution
   ![alt text](image-54.png)

# 18 March

## A new where operator

1. Initial query
   ![alt text](image-55.png)

2. Solution
   ![alt text](image-57.png)

# 19 March

## Some method

1. Query
   ![alt text](image-58.png)

2. Solution
   ![alt text](image-59.png)

# 25 March

## Probably too much about correlated subqueries

1. Query
   ![alt text](image-60.png)

2. To understand nested coorelated queries, Consider them like nested for loop.
   ![alt text](image-61.png)

3. In the above diagram, Image i=0 and j=0;
4. Solution
   ![alt text](image-62.png)

# 28 March

## More on correlated subqueries

1. Query
   ![alt text](image-63.png)

2. Solution
   ![alt text](image-64.png)

## A select without a from

1. Here is the query
   ![alt text](image-65.png)

2. Use case
   ![alt text](image-66.png)

# 1 April

## Selecting distinct values

1. Distinct gives the unique values for a column.
   ![alt text](image-67.png)
2. To count the number of unique departments
   ![alt text](image-68.png)

## The Greatest value in a list

1. To find the greatest value
   ![alt text](image-69.png)
2. Where we might use this function
   ![alt text](image-70.png)
3. Live example
   ![alt text](image-71.png)

## The least value in a list

1. Here is the example
   ![alt text](image-72.png)
2. Where we would use the least
   ![alt text](image-73.png)
3. Example
   ![alt text](image-74.png)

# 4 April

## The case keyword(Not important for practical usage we want to handle this on code level)

1. Query
   ![alt text](image-75.png)

2. Solution
   ![alt text](image-76.png)

# 5 April

## Thinking about validation

# 8 April

## Thinking about validation

1. Discussion about adding negative price to the database when user directly interacting with database.

## Creating and viewing tables in PGadmin

1. Create product table in pgadmin
   ![alt text](image-77.png)

2. Insert one row
   ![alt text](image-78.png)
