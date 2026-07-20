# <img src="https://images.mindcloud.co/apps/icons/change-crab_1774901586465.png" alt="ChangeCrab logo" width="28" height="28"> ChangeCrab: Universal API

ChangeCrab lets teams manage product changelogs, categories, and posts through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/changeCrab/latest
- **Category:** Support / Customer Success
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://changecrab.com
- **Vendor API docs:** https://changecrab.com/api/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Changelog](actions/get-changelog.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/get-changelog?connectionId=$CONNECTION_ID&id=e.g.%20product-updates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories for a changelog from ChangeCrab. |

### Changelog

| Action | Method | Description |
| --- | --- | --- |
| [Create Changelog](actions/create-changelog.md) | POST | Creates a new changelog in ChangeCrab. |
| [Delete Changelog](actions/delete-changelog.md) | DELETE | Deletes an existing changelog from ChangeCrab. |
| [Get Changelog](actions/get-changelog.md) | GET | Retrieves a changelog from ChangeCrab. |
| [List Changelogs](actions/list-changelogs.md) | GET | Retrieves changelogs from ChangeCrab. |
| [Update Changelog](actions/update-changelog.md) | PUT | Updates an existing changelog in ChangeCrab. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new post in ChangeCrab. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post from ChangeCrab. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts for a changelog from ChangeCrab. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post in ChangeCrab. |

