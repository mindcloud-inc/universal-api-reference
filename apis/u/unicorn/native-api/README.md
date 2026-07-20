# Unicorn: Native API Reference

A consolidated summary of Unicorn's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://help.unicornplatform.com/en/category/api-1dkmw9e/
- **API base URL:** `https://api.unicornplatform.com/api/v1`

## Authentication

### API Key

Use the Unicorn Platform API key from Blog settings. Unicorn injects this credential into endpoint path parameters on the write actions.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.unicornplatform.com/en/article/how-to-connect-seobot-publish-and-unpublish-seobot-post-1h7pub1/)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Blog Post](actions/create-blog-post.md) | `POST /blog_posts/seobot_hook/:seobot_api_key/:seobot_post_id` | [docs](https://help.unicornplatform.com/en/article/create-blog-post-c36bv7/) |
| [Delete Blog Post](actions/delete-blog-post.md) | `DELETE /blog_posts/seobot_hook/:seobot_api_key/:seobot_post_id` | [docs](https://help.unicornplatform.com/en/article/delete-blog-post-ns3ki7/) |
| [List Blog Posts](actions/list-blog-posts.md) | `GET /blog_posts/get_posts/:subdomain` | [docs](https://help.unicornplatform.com/en/article/get-blog-posts-1f5xjft/) |
| [Update Blog Post](actions/update-blog-post.md) | `PATCH /blog_posts/seobot_hook/:seobot_api_key/:seobot_post_id` | [docs](https://help.unicornplatform.com/en/article/edit-blog-post-1epmmaf/) |
