# <img src="https://images.mindcloud.co/apps/icons/useless-facts_1785420706369.png" alt="Useless Facts logo" width="28" height="28"> Useless Facts: Universal API

Get random and daily useless facts in English or German.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uselessFacts/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://uselessfacts.jsph.pl/
- **Vendor API docs:** https://uselessfacts.jsph.pl/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Random Useless Fact](actions/fetch-random-useless-fact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uselessFacts/latest/actions/fetch-random-useless-fact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Useless Fact

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Random Useless Fact](actions/fetch-random-useless-fact.md) | GET |  |
| [Fetch Useless Fact of the Day](actions/fetch-useless-fact-of-the-day.md) | GET |  |

