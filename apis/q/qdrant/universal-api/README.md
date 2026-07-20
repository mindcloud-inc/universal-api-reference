# <img src="https://images.mindcloud.co/apps/icons/qdrant_1776079839602.png" alt="Qdrant logo" width="28" height="28"> Qdrant: Universal API

Qdrant: Store, search, and manage vector collections

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qdrant/latest
- **Category:** IT Operations / Database
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://qdrant.tech
- **Vendor API docs:** https://api.qdrant.tech/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Collections](actions/list-collections.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qdrant/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Collections](actions/list-collections.md) | GET | Retrieves all existing collections from Qdrant. |

