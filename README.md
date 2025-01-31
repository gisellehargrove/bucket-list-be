# Bucket List API

## Base URL: https://bucket-list-be.herokuapp.com/

---

##Endpoints

### GET /api/users

    -returns all users

### GET /api/user

    -returns a user currently logged in

### GET /api/user/:id

    -returns a user by id

### GET /api/user/:user_id/items

    -returns all bucket list items for user_id

### GET /api/item/:id'

    -returns bucket list item for id

### GET /api/item/:item_id/posts

    -returns all posts for item_id


### GET /api/item/post/:id

    -returns a post for id

### GET /api/item/post/:post_id/images

    -returns an all images for post_id

### GET /api/item/post/image/:id

    -returns image for id 

### POST /api/register

    -input:
        -name -Required
        -email -Required
        -password -Required

    -returns { message: "User creates", token: "user token" }

### POST /api/login

    -input:
        -email -Required
        -password -Required

    -returns { message: "Logged in", token: "user token" }

### POST /api/item

    -input:
        -user_id -Required
        -description -Required

    -returns id of new item

### POST /api/item/post

    -input:
        -item_id -Required
        -message -Required

    -returns id of new post

### POST /api/item/post/image

    -input:
        -post_id -Required
        -image 
        -url

    image and url are not required so you can choose how to store an image.

    -returns id of new post

### PUT /api/item/:id

    -input:
        -user_id -Required
        -description -Required

     -returns id of updated item

### PUT /api/item/post/:id

    -input:
        -item_id -Required
        -message -Required

    -returns id of updated post

### PUT /item/post/image/:id

    -input:
        -post_id -Required
        -image 
        -url

    -returns id of updated image

### DELETE /api/item/:id

    -returns deletes an item by id and returns { message: "deleted id id# " }

### DELETE /api/item/post/:id

    -returns deletes an post by id and returns { message: "deleted id id# " }


### DELETE /item/post//image/:id

    -returns deletes an image by id and returns { message: "deleted id id# " }