# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423647989.png" alt="Dev Excuses logo" width="28" height="28"> Dev Excuses: Universal API

Retrieve a random developer excuse in the default English or documented French locale. Data is supplied by the Dev Excuses API project.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/devExcuses/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Developer Excuse](actions/get-random-developer-excuse.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devExcuses/latest/actions/get-random-developer-excuse?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Developer Excuse

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Developer Excuse](actions/get-random-developer-excuse.md) | GET |  |

