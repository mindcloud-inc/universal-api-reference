# <img src="https://images.mindcloud.co/apps/icons/devto_1776273317960.png" alt="Dev.to logo" width="28" height="28"> Dev.to: Universal API

Publish and manage DEV Community articles, read public content, inspect users and organizations, and work with comments, tags, reactions, reading lists, podcasts, and videos through the Forem API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/devto/latest
- **Category:** Marketing / Social Media
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dev.to
- **Vendor API docs:** https://developers.forem.com/api/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a Dev.to comment and its descendant comments by ID. |
| [List Article Comments](actions/list-article-comments.md) | GET | Lists threaded comments for a Dev.to article or podcast episode. |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [Get Article](actions/get-article.md) | GET | Retrieves a published Dev.to article by ID. |
| [Get Article By Path](actions/get-article-by-path.md) | GET | Retrieves a published Dev.to article by username and slug path. |
| [List All My Articles](actions/list-all-my-articles.md) | GET | Lists all Dev.to articles for the authenticated user. |
| [List Latest Articles](actions/list-latest-articles.md) | GET | Lists published Dev.to articles sorted by newest publish date. |
| [List My Articles](actions/list-my-articles.md) | GET | Lists the authenticated user's published Dev.to articles. |
| [List My Draft Articles](actions/list-my-draft-articles.md) | GET | Lists the authenticated user's unpublished Dev.to articles. |
| [List My Published Articles](actions/list-my-published-articles.md) | GET | Lists the authenticated user's published Dev.to articles. |
| [List Organization Articles](actions/list-organization-articles.md) | GET | Lists articles for a Dev.to organization. |
| [List Published Articles](actions/list-published-articles.md) | GET | Lists published articles in Dev.to. |
| [List Reading List](actions/list-reading-list.md) | GET | Lists articles saved to the authenticated user's Dev.to reading list. |
| [Publish Article](actions/publish-article.md) | POST | Publishes a new article in Dev.to. |
| [Unpublish Article](actions/unpublish-article.md) | PUT | Unpublishes a Dev.to article by ID. |
| [Update Article](actions/update-article.md) | PUT | Updates an existing Dev.to article by ID. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves a Dev.to organization by username. |

### Reactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Reaction](actions/create-reaction.md) | POST | Creates a reaction to an article, comment, or user in Dev.to. |
| [Toggle Reaction](actions/toggle-reaction.md) | PUT | Toggles the authenticated user's reaction to an article, comment, or user in Dev.to. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Followed Tags](actions/list-followed-tags.md) | GET | Lists the tags followed by the authenticated Dev.to user. |
| [List Tags](actions/list-tags.md) | GET | Lists tags that can be used on Dev.to articles. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated Dev.to user. |
| [Get User](actions/get-user.md) | GET | Retrieves a Dev.to user by ID or username. |
| [List Followers](actions/list-followers.md) | GET | Lists the followers of the authenticated Dev.to user. |
| [List Organization Users](actions/list-organization-users.md) | GET | Lists users in a Dev.to organization. |

