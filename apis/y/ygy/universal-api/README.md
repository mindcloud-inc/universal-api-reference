# <img src="https://images.mindcloud.co/apps/icons/ygy_1775573472085.png" alt="y.gy logo" width="28" height="28"> y.gy: Universal API

Create, manage, and organize short links and tags

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ygy/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://y.gy
- **Vendor API docs:** https://app.y.gy/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Links](actions/list-links.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ygy/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Short Link](actions/create-short-link.md) | POST | Creates a new short link in y.gy. |
| [Delete Short Link](actions/delete-short-link.md) | DELETE | Deletes an existing short link from y.gy. |
| [Get Short Link](actions/get-short-link.md) | GET | Retrieves a short link from y.gy. |
| [List Links](actions/list-links.md) | GET | Retrieves short links from y.gy. |
| [Update Short Link](actions/update-short-link.md) | PUT | Updates an existing short link in y.gy. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in y.gy. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from y.gy. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from y.gy. |

