# <img src="https://images.mindcloud.co/apps/icons/screenshotfyi_1774558315343.png" alt="screenshot.fyi logo" width="28" height="28"> screenshot.fyi: Universal API

Capture premium-quality screenshots of public web pages with a single REST API call.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/screenshotfyi/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.screenshot.fyi/
- **Vendor API docs:** https://www.screenshot.fyi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Take Screenshot](actions/take-screenshot.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenshotfyi/latest/actions/take-screenshot?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Take Screenshot](actions/take-screenshot.md) | GET |  |

