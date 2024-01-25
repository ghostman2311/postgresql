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
