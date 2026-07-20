# Delete Blog Post with Unicorn

Deletes an existing blog post from Unicorn.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/blog_posts/seobot_hook/:seobot_api_key/:seobot_post_id`
- **Base URL:** `https://api.unicornplatform.com/api/v1`
- **Official documentation:** [Delete Blog Post](https://help.unicornplatform.com/en/article/delete-blog-post-ns3ki7/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `seobot_post_id` | path | `string` | yes | The unique string identifier assigned when the post was created. |
