# Create Blog Post with Unicorn

Creates a blog post in Unicorn.

## Endpoint

- **Method:** `POST`
- **Path:** `/blog_posts/seobot_hook/:seobot_api_key/:seobot_post_id`
- **Base URL:** `https://api.unicornplatform.com/api/v1`
- **Official documentation:** [Create Blog Post](https://help.unicornplatform.com/en/article/create-blog-post-c36bv7/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `seobot_post_id` | path | `string` | yes | A string identifier that is unique across all Unicorn blog posts. |
| `slug` | body | `string` | yes | Path of the new blog post. Must be unique across the blog. |
| `html` | body | `string` | yes | HTML content of the new post. |
| `headline` | body | `string` | yes | Meta title. |
| `metaDescription` | body | `string` | yes | Meta description. |
| `metaKeywords` | body | `string` | yes | Meta keywords. Unicorn notes that these are not used anywhere at the moment. |
| `thumbnailUrl` | body | `string` | yes | Source URL of the post's thumbnail image. |
| `createdAt` | body | `string` | yes | Publication date in YYYY-MM-DDTHH:MM:SS format. |
| `published` | body | `boolean` | yes | Whether the new post is publicly available. |
| `directory` | body | `string` | no | Optional subdirectory for the new blog post, for example nocode. |
| `is_deleted` | body | `boolean` | no | Mark the post as deleted. |
