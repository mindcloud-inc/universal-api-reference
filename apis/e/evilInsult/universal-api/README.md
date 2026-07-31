# <img src="https://images.mindcloud.co/apps/icons/evil_1785427022391.png" alt="Evil Insult logo" width="28" height="28"> Evil Insult: Universal API

Generate intentionally insulting/offensive phrases in a selected supported language and response format.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/evilInsult/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://evilinsult.com/
- **Vendor API docs:** https://evilinsult.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Insult (JSON)](actions/generate-insult-json.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evilInsult/latest/actions/generate-insult-json?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Generate Insult (JSON)](actions/generate-insult-json.md) | GET |  |
| [Generate Insult (Text)](actions/generate-insult-text.md) | GET |  |
| [Generate Insult (XML)](actions/generate-insult-xml.md) | GET |  |

