# EONET: List RSS Event Feed Items

Retrieves RSS event feed items from EONET.

```
GET https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-rss-event-feed-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EONET `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-rss-event-feed-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-rss-event-feed-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | Filter events by status: open, closed, or all. |
| `source` | string | no | Filter by source ID. Comma-separated values act as OR. |
| `category` | string | no | Filter by category ID. Comma-separated values act as OR. |
| `days` | number | no | Return events from the last N days, including today. |
| `start` | date | no | Return events on or after this date (YYYY-MM-DD). |
| `end` | date | no | Return events on or before this date (YYYY-MM-DD). |
| `bbox` | string | no | Bounding box as upper-left lon,lat and lower-right lon,lat. |
| `magId` | string | no | Filter by magnitude type ID. |
| `magMin` | number | no | Minimum magnitude value. |
| `magMax` | number | no | Maximum magnitude value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "description": "string",
      "guid": "string",
      "link": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `description` | string |  |
| `guid` | string |  |
| `link` | string |  |
| `title` | string |  |

## Native endpoint

Through the native EONET API, this operation is `GET /events/rss` (base URL `https://eonet.gsfc.nasa.gov/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rss-event-feed-items.md) for the provider-specific parameters and requirements.

