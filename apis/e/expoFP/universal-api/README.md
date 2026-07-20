# <img src="https://images.mindcloud.co/apps/icons/expo-fp_1776279483811.png" alt="ExpoFP logo" width="28" height="28"> ExpoFP: Universal API

Create, update, and manage ExpoFP expo data including exhibitors, booths, categories, extras, sessions, tracks, speakers, and floor-plan conversions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/expoFP/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://expofp.com
- **Vendor API docs:** https://developer.expofp.com/guide/json-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List All Expos](actions/list-all-expos.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expoFP/latest/actions/list-all-expos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List All Expos](actions/list-all-expos.md) | GET |  |

