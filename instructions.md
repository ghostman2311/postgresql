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
