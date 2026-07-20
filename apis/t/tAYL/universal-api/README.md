# <img src="https://images.mindcloud.co/apps/icons/tayl-square-icon_1775582027427.png" alt="TAYL logo" width="28" height="28"> TAYL: Universal API

Turn websites and text content into spoken audio tales and podcast-ready listening items through the TAYL backend.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tAYL/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tayl.app
- **Vendor API docs:** https://my.tayl.app/create/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tales](actions/list-tales.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/list-tales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Tale From Text](actions/create-tale-from-text.md) | POST |  |
| [Create Tale From URL](actions/create-tale-from-url.md) | POST |  |
| [List Tales](actions/list-tales.md) | GET |  |

