# <img src="https://images.mindcloud.co/apps/icons/zillow-zestimates_1776964183963.png" alt="Zillow Zestimates logo" width="28" height="28"> Zillow Zestimates: Universal API

Bridge-hosted Zillow Zestimates access. Requires a Bridge account and approved Zestimate datasets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zillowZestimates/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zillowgroup.com/developers/api/zestimate/zestimates-api/
- **Vendor API docs:** https://bridgedataoutput.com/docs/platform

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List zestimates](actions/list-zestimates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowZestimates/latest/actions/list-zestimates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List zestimates](actions/list-zestimates.md) | GET | Retrieves current property, rental, and foreclosure Zestimates from Zillow. |

