# Update Blog Post with Unicorn

Updates an existing blog post in Unicorn.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/blog_posts/seobot_hook/:seobot_api_key/:seobot_post_id`
- **Base URL:** `https://api.unicornplatform.com/api/v1`
- **Official documentation:** [Update Blog Post](https://help.unicornplatform.com/en/article/edit-blog-post-1epmmaf/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `seobot_post_id` | path | `string` | yes | The unique string identifier assigned when the post was created. |
| `slug` | body | `string` | no | Path of the updated blog post. Must be unique across the blog when changed. |
| `html` | body | `string` | no | HTML content of the updated post. |
| `headline` | body | `string` | no | Meta title. |
| `metaDescription` | body | `string` | no | Meta description. |
| `metaKeywords` | body | `string` | no | Meta keywords. Unicorn notes that these are not used anywhere at the moment. |
| `thumbnailUrl` | body | `string` | no | Source URL of the post's thumbnail image. |
| `createdAt` | body | `string` | no | Publication date in YYYY-MM-DDTHH:MM:SS format. |
| `published` | body | `boolean` | no | Whether the updated post is publicly available. |
| `directory` | body | `string` | no | Optional subdirectory for the blog post, for example nocode. |
| `is_deleted` | body | `boolean` | no | Mark the post as deleted. |
