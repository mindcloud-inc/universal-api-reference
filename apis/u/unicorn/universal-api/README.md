# <img src="https://images.mindcloud.co/apps/icons/unicorn_1775492523990.png" alt="Unicorn logo" width="28" height="28"> Unicorn: Universal API

Unicorn Platform is an AI website builder that helps founders quickly create websites, blogs, directories, and landing pages without design or development skills.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/unicorn/latest
- **Category:** Marketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://unicornplatform.com
- **Vendor API docs:** https://help.unicornplatform.com/en/category/api-1dkmw9e/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Blog Posts](actions/list-blog-posts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/list-blog-posts?connectionId=$CONNECTION_ID&subdomain=your-blog-subdomain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Create Blog Post](actions/create-blog-post.md) | POST | Creates a blog post in Unicorn. |
| [Delete Blog Post](actions/delete-blog-post.md) | DELETE | Deletes an existing blog post from Unicorn. |
| [List Blog Posts](actions/list-blog-posts.md) | GET | Retrieves published blog posts from Unicorn. |
| [Update Blog Post](actions/update-blog-post.md) | PUT | Updates an existing blog post in Unicorn. |

