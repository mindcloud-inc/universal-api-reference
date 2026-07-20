# <img src="https://images.mindcloud.co/apps/icons/blog-in_1775234167654.png" alt="BlogIn logo" width="28" height="28"> BlogIn: Universal API

Share internal news, knowledge, and updates across your company

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blogIn/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.blogin.co
- **Vendor API docs:** https://blogin.co/api/rest/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Members](actions/list-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in BlogIn. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes an existing category from BlogIn. |
| [Get Category](actions/get-category.md) | GET | Retrieves a specific category from BlogIn. |
| [List Categories](actions/list-categories.md) | GET | Retrieves all categories from BlogIn. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in BlogIn. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Member](actions/create-member.md) | POST | Creates a new member in BlogIn. |
| [Delete Member](actions/delete-member.md) | DELETE | Deletes an existing member from BlogIn. |
| [Get Member](actions/get-member.md) | GET | Retrieves a specific member from BlogIn. |
| [List Members](actions/list-members.md) | GET | Retrieves all members from BlogIn. |
| [Update Member](actions/update-member.md) | PUT | Updates an existing member in BlogIn. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page in BlogIn. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes an existing page from BlogIn. |
| [Get Page](actions/get-page.md) | GET | Retrieves a specific page from BlogIn. |
| [List Pages](actions/list-pages.md) | GET | Retrieves all pages from BlogIn. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in BlogIn. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new post in BlogIn. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post from BlogIn. |
| [Get Post](actions/get-post.md) | GET | Retrieves a specific post from BlogIn. |
| [List Posts](actions/list-posts.md) | GET | Retrieves all posts from BlogIn. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post in BlogIn. |

### Post Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Post Comment](actions/add-post-comment.md) | POST | Adds a comment to a BlogIn post. |
| [Delete Post Comment](actions/delete-post-comment.md) | DELETE | Deletes a comment from a BlogIn post. |
| [List Post Comments](actions/list-post-comments.md) | GET | Retrieves comments for a BlogIn post. |
| [Update Post Comment](actions/update-post-comment.md) | PUT | Updates a comment on a BlogIn post. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Finds matching content in BlogIn by search terms. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves all tags from BlogIn. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Delete Team](actions/delete-team.md) | DELETE | Deletes an existing team from BlogIn. |
| [Get Team](actions/get-team.md) | GET | Retrieves a specific team from BlogIn. |
| [List Teams](actions/list-teams.md) | GET | Retrieves all teams from BlogIn. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in BlogIn. |

