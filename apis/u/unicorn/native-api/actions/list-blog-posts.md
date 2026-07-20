# List Blog Posts with Unicorn

Retrieves published blog posts from Unicorn.

## Endpoint

- **Method:** `GET`
- **Path:** `/blog_posts/get_posts/:subdomain`
- **Base URL:** `https://api.unicornplatform.com/api/v1`
- **Official documentation:** [List Blog Posts](https://help.unicornplatform.com/en/article/get-blog-posts-1f5xjft/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subdomain` | path | `string` | yes | The default subdomain of your Unicorn blog website. |
| `amount` | query | `number` | no | The number of posts to return. |
| `exclude_post_content` | query | `boolean` | no | Exclude the post body fields from the response when true. |
