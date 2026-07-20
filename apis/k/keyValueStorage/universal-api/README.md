# Key Value Storage: Universal API

Key Value Storage through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/keyValueStorage/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Value](actions/get-value.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/get-value?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Value

| Action | Method | Description |
| --- | --- | --- |
| [Get Value](actions/get-value.md) | GET |  |
| [Set Value](actions/set-value.md) | PUT |  |

