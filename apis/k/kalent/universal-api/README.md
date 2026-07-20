# <img src="https://images.mindcloud.co/apps/icons/kalent-icon-square_1775488497144.png" alt="Kalent logo" width="28" height="28"> Kalent: Universal API

Search millions of professional profiles with Kalent's live talent search API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kalent/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kalent.ai
- **Vendor API docs:** https://docs.kalent.ai/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Talents](actions/search-talents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kalent/latest/actions/search-talents?connectionId=$CONNECTION_ID&filters%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [Search Talents](actions/search-talents.md) | GET |  |

