# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-birdie-so-48x48_1776089234465.png" alt="Birdie Screen Recording logo" width="28" height="28"> Birdie Screen Recording: Universal API

Manage Birdie recordings and provision workspace users

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/birdieScreenRecording/latest
- **Category:** Communication / Video Communications
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.birdie.so
- **Vendor API docs:** https://docs.birdie.so/birdie-docs/birdie-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Recordings](actions/list-recordings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/birdieScreenRecording/latest/actions/list-recordings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [List Recordings](actions/list-recordings.md) | GET | Retrieves recordings from Birdie Screen Recording. |

