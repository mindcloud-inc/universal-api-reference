# <img src="https://images.mindcloud.co/apps/icons/buzzsprout_1776255959219.png" alt="Buzzsprout logo" width="28" height="28"> Buzzsprout: Universal API

Manage Buzzsprout podcasts and episodes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/buzzsprout/latest
- **Category:** Website & App Building / CMS
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.buzzsprout.com
- **Vendor API docs:** https://github.com/buzzsprout/buzzsprout-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Podcasts](actions/list-podcasts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buzzsprout/latest/actions/list-podcasts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Podcast

| Action | Method | Description |
| --- | --- | --- |
| [List Podcasts](actions/list-podcasts.md) | GET | Retrieves podcasts from Buzzsprout. |

