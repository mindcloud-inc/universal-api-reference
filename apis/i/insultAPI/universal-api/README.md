# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423607365.png" alt="Insult API logo" width="28" height="28"> Insult API: Universal API

Insult API through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/insultAPI/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Adjective](actions/get-adjective.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insultAPI/latest/actions/get-adjective?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Adjective

| Action | Method | Description |
| --- | --- | --- |
| [Get Adjective](actions/get-adjective.md) | GET |  |
| [Get Adjective HTML](actions/get-adjective-html.md) | GET |  |
| [Get Adjective JSON](actions/get-adjective-json.md) | GET |  |

### Insult

| Action | Method | Description |
| --- | --- | --- |
| [Get Insult](actions/get-insult.md) | GET |  |
| [Get Insult HTML](actions/get-insult-html.md) | GET |  |
| [Get Insult JSON](actions/get-insult-json.md) | GET |  |

