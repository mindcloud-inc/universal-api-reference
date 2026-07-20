# <img src="https://images.mindcloud.co/apps/icons/confluence_1773349792413.png" alt="Confluence logo" width="28" height="28"> Confluence: Universal API

Create, update, and organize Confluence pages, spaces, and comments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/confluenceCloud/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.atlassian.com/software/confluence
- **Vendor API docs:** https://developer.atlassian.com/cloud/confluence/rest/v2/intro/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accessible Resources](actions/list-accessible-resources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-accessible-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Accessible Resource

| Action | Method | Description |
| --- | --- | --- |
| [List Accessible Resources](actions/list-accessible-resources.md) | GET | Retrieves accessible Confluence sites for an OAuth app. |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment](actions/get-attachment.md) | GET | Retrieves an existing attachment from Confluence. |
| [List Attachments For Page](actions/list-attachments-for-page.md) | GET | Retrieves attachments for a Confluence page. |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Create Attachment For Page](actions/create-attachment-for-page.md) | POST | Creates a new attachment for a Confluence page. |

### Blog Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Blog Post](actions/create-blog-post.md) | POST | Creates a new blog post in Confluence. |
| [Delete Blog Post](actions/delete-blog-post.md) | DELETE | Deletes an existing blog post from Confluence. |
| [Get Blog Post](actions/get-blog-post.md) | GET | Retrieves a blog post from Confluence. |
| [List Blog Posts](actions/list-blog-posts.md) | GET | Retrieves a list of blog posts from Confluence. |
| [List Blog Posts In Space](actions/list-blog-posts-in-space.md) | GET | Retrieves blog posts from a Confluence space. |
| [Update Blog Post](actions/update-blog-post.md) | PUT | Updates an existing blog post in Confluence. |

### Footer Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Footer Comment](actions/create-footer-comment.md) | POST | Creates a new footer comment in Confluence. |
| [Delete Footer Comment](actions/delete-footer-comment.md) | DELETE | Deletes an existing footer comment from Confluence. |
| [Get Footer Comment](actions/get-footer-comment.md) | GET | Retrieves a footer comment from Confluence. |
| [List Footer Comments](actions/list-footer-comments.md) | GET | Retrieves a list of footer comments from Confluence. |
| [List Footer Comments For Page](actions/list-footer-comments-for-page.md) | GET | Retrieves footer comments for a Confluence page. |
| [Update Footer Comment](actions/update-footer-comment.md) | PUT | Updates an existing footer comment in Confluence. |

### Inline Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Inline Comments For Page](actions/list-inline-comments-for-page.md) | GET | Retrieves inline comments for a Confluence page. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [List Labels For Page](actions/list-labels-for-page.md) | GET | Retrieves labels for a Confluence page. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page in Confluence. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes an existing page from Confluence. |
| [Get Page](actions/get-page.md) | GET | Retrieves an existing page from Confluence. |
| [List Pages](actions/list-pages.md) | GET | Retrieves a list of pages from Confluence. |
| [List Pages In Space](actions/list-pages-in-space.md) | GET | Retrieves pages from a Confluence space. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in Confluence. |
| [Update Page Title](actions/update-page-title.md) | PUT | Updates an existing page title in Confluence. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Get Space](actions/get-space.md) | GET | Retrieves an existing space from Confluence. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves a list of spaces from Confluence. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET | Retrieves an existing task from Confluence. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from Confluence. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Confluence. |

