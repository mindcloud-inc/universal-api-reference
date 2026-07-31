# <img src="https://images.mindcloud.co/apps/icons/yes-no_1785359543222.png" alt="Yes/No logo" width="28" height="28"> Yes/No: Universal API

Get random or forced yes/no/maybe decisions with a GIF image URL.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yesNo/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://yesno.wtf/
- **Vendor API docs:** https://yesno.wtf/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Answer](actions/get-answer.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yesNo/latest/actions/get-answer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Decision

| Action | Method | Description |
| --- | --- | --- |
| [Get Answer](actions/get-answer.md) | GET |  |

