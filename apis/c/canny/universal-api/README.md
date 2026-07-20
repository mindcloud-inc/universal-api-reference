# <img src="https://images.mindcloud.co/apps/icons/canny_1773694782306.png" alt="Canny logo" width="28" height="28"> Canny: Universal API

Manage feedback boards, posts, comments, votes, and users

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/canny/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://canny.io
- **Vendor API docs:** https://developers.canny.io/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Boards](actions/list-boards.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-boards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Board

| Action | Method | Description |
| --- | --- | --- |
| [List Boards](actions/list-boards.md) | GET | Retrieves all available boards from Canny. |
| [Retrieve Board](actions/retrieve-board.md) | GET | Retrieves a single board from Canny. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in Canny. |
| [List Categories](actions/list-categories.md) | GET | Retrieves all available categories from Canny. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Canny. |
| [List Comments](actions/list-comments.md) | GET | Retrieves all available comments from Canny. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves all available companies from Canny. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Canny. |

### Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Entry](actions/create-entry.md) | POST | Creates a new entry in Canny. |
| [List Entries](actions/list-entries.md) | GET | Retrieves all available entries from Canny. |

### Idea

| Action | Method | Description |
| --- | --- | --- |
| [List Ideas](actions/list-ideas.md) | GET | Retrieves all available ideas from Canny. |
| [Merge Idea](actions/merge-idea.md) | PUT | Merges an idea into another idea in Canny. |
| [Retrieve Idea](actions/retrieve-idea.md) | GET | Retrieves a single idea from Canny. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Change Post Category](actions/change-post-category.md) | PUT | Updates a post category in Canny. |
| [Change Post Status](actions/change-post-status.md) | PUT | Updates a post status in Canny. |
| [Create Post](actions/create-post.md) | POST | Creates a new post in Canny. |
| [List Posts](actions/list-posts.md) | GET | Retrieves all available posts from Canny. |
| [Retrieve Post](actions/retrieve-post.md) | GET | Retrieves a single post from Canny. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post in Canny. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Canny. |
| [List Tags](actions/list-tags.md) | GET | Retrieves all available tags from Canny. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update User](actions/create-or-update-user.md) | PUT | Creates or updates a user in Canny. |
| [List Users](actions/list-users.md) | GET | Retrieves all available users from Canny. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves a single user from Canny. |

