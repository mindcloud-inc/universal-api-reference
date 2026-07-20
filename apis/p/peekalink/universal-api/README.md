# <img src="https://images.mindcloud.co/apps/icons/peekalink_1775829106546.png" alt="Peekalink logo" width="28" height="28"> Peekalink: Universal API

Generate enriched link previews and metadata for URLs using Peekalink's Link Preview API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/peekalink/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.peekalink.io/
- **Vendor API docs:** https://docs.peekalink.io/quickstart

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get a Link Preview](actions/get-link-preview.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peekalink/latest/actions/get-link-preview?connectionId=$CONNECTION_ID&link=https%3A%2F%2Fwww.peekalink.io%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get a Link Preview](actions/get-link-preview.md) | GET | Retrieves a link preview from Peekalink. |

