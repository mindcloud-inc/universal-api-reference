# <img src="https://images.mindcloud.co/apps/icons/plasmic-icon-padded_1776183528177.png" alt="Plasmic logo" width="28" height="28"> Plasmic: Universal API

Access Plasmic CMS collections to query, count, create, update, and delete content rows through the official Plasmic CMS REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/plasmic/latest
- **Category:** IT Operations / Database
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.plasmic.app/
- **Vendor API docs:** https://docs.plasmic.app/learn/plasmic-cms-api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Count Items](actions/count-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/count-items?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Count Draft Items](actions/count-draft-items.md) | GET | Counts draft items in Plasmic CMS. |
| [Count Items](actions/count-items.md) | GET | Counts items in Plasmic CMS. |
| [Create Items](actions/create-items.md) | POST | Creates items in Plasmic CMS. |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an item from Plasmic CMS. |
| [Publish Item](actions/publish-item.md) | PUT | Publishes an item in Plasmic CMS. |
| [Query Draft Items](actions/query-draft-items.md) | GET | Retrieves draft items from Plasmic CMS. |
| [Query Items](actions/query-items.md) | GET | Retrieves items from Plasmic CMS. |
| [Update Item](actions/update-item.md) | PUT | Updates an item in Plasmic CMS. |

