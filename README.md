![logo](https://res.cloudinary.com/placeiknow/image/upload/c_scale,w_200/v1503588668/logo_shhvcy.png)
# Image Microservice

This microservice accepts messages from a RabbitMQ broker with queue name "images".

## Accepted Messages

**Remove image from Cloudinary**

```javascript
{
  function: 'REMOVE_CLOUDINARY_IMAGE',
  cloudinaryPublicId: '<cloudinary_public_id>',
};
```
Removes the `cloudinary_public_id` from the Cloudinary media library.

Currently used:
- When a user is uploading a new avatar, to destroy the temporary image used when cropping the uploaded image into a square.

## Copyright
&copy; 2018 Shaun Jacobsen. All Rights Reserved.
