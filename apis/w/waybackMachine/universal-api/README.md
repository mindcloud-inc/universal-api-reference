# <img src="https://images.mindcloud.co/apps/icons/wbm-icon_1777579394727.png" alt="Wayback Machine logo" width="28" height="28"> Wayback Machine: Universal API

Find and inspect archived web page captures

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/waybackMachine/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://web.archive.org/
- **Vendor API docs:** https://archive.org/help/wayback_api.php

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check URL Availability](actions/check-url-availability.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/check-url-availability?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Archived Snapshot Availability

| Action | Method | Description |
| --- | --- | --- |
| [Check URL Availability](actions/check-url-availability.md) | GET | Retrieves archived snapshot availability for a URL in Wayback Machine. |
| [Get Closest Capture By Timestamp](actions/get-closest-capture-by-timestamp.md) | GET | Retrieves the closest archived capture to a timestamp in Wayback Machine. |

### Cdx Capture

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest CDX Capture](actions/get-latest-cdx-capture.md) | GET | Retrieves the latest archived capture from the Wayback Machine CDX index. |
| [Get Oldest CDX Capture](actions/get-oldest-cdx-capture.md) | GET | Retrieves the oldest archived capture from the Wayback Machine CDX index. |
| [Search CDX Captures](actions/search-cdx-captures.md) | GET | Finds archived captures in the Wayback Machine CDX index. |

### Cdx Page Count

| Action | Method | Description |
| --- | --- | --- |
| [Get CDX Page Count](actions/get-cdx-page-count.md) | GET | Retrieves the CDX result page count for a Wayback query. |

