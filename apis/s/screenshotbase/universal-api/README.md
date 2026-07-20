# <img src="https://images.mindcloud.co/apps/icons/screenshotbase_1774389590902.png" alt="Screenshotbase logo" width="28" height="28"> Screenshotbase: Universal API

Render websites and capture screenshots with Screenshotbase

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/screenshotbase/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://screenshotbase.com
- **Vendor API docs:** https://screenshotbase.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check API Status](actions/check-api-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenshotbase/latest/actions/check-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Quota Status

| Action | Method | Description |
| --- | --- | --- |
| [Check API Status](actions/check-api-status.md) | GET | Retrieves current quota status from Screenshotbase. |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Take Website Screenshot](actions/take-website-screenshot.md) | POST | Captures a website screenshot with Screenshotbase. |

