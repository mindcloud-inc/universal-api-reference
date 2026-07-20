# <img src="https://images.mindcloud.co/apps/icons/dropmark_1776177978003.png" alt="Dropmark logo" width="28" height="28"> Dropmark: Universal API

Read-only wrapper for the Dropmark Feed API, covering activity feeds and collection exports for a specific Dropmark subdomain.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dropmark/latest
- **Category:** Content & Files / Storage
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dropmark.com
- **Vendor API docs:** https://support.dropmark.com/article/96-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Activity](actions/get-activity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-activity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | GET |  |

### Activity Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity Feed](actions/get-activity-feed.md) | GET |  |

### Activity Rss

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity RSS](actions/get-activity-rss.md) | GET |  |

### Activity Xml

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity XML](actions/get-activity-xml.md) | GET |  |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection](actions/get-collection.md) | GET |  |

### Collection Csv

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection CSV](actions/get-collection-csv.md) | GET |  |

### Collection Export

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection Export](actions/get-collection-export.md) | GET |  |

### Collection Pls

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection PLS](actions/get-collection-pls.md) | GET |  |

### Collection Rss

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection RSS](actions/get-collection-rss.md) | GET |  |

### Collection Xml

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection XML](actions/get-collection-xml.md) | GET |  |

