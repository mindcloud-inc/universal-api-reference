# <img src="https://images.mindcloud.co/apps/icons/cat-facts_1785360826062.png" alt="Cat Facts logo" width="28" height="28"> Cat Facts: Universal API

Retrieve cat facts and browse cat breed details from the Cat Fact API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/catFacts/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://catfact.ninja
- **Vendor API docs:** https://catfact.ninja/docs?api-docs.json

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Fact](actions/get-random-fact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/get-random-fact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Cat Breed

| Action | Method | Description |
| --- | --- | --- |
| [List Breeds](actions/list-breeds.md) | GET |  |

### Cat Fact

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Fact](actions/get-random-fact.md) | GET |  |
| [List Facts](actions/list-facts.md) | GET |  |

