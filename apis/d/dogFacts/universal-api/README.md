# <img src="https://images.mindcloud.co/apps/icons/dog-facts_1785420651699.png" alt="Dog Facts logo" width="28" height="28"> Dog Facts: Universal API

Retrieve one or more random dog facts from Dog API v2.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dogFacts/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dogapi.dog/
- **Vendor API docs:** https://dogapi.dog/docs/api-v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Dog Facts](actions/list-dog-facts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dogFacts/latest/actions/list-dog-facts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Dog Fact

| Action | Method | Description |
| --- | --- | --- |
| [List Dog Facts](actions/list-dog-facts.md) | GET |  |

