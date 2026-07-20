# EONET: List Events

Retrieves events from EONET.

```
GET https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EONET `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-events?${params}`, {
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
| `status` | string | no | Event status filter: open, closed, or all. |
| `source` | string | no | Comma-separated EONET source IDs. |
| `category` | string | no | Comma-separated EONET category IDs. |
| `days` | number | no | Number of prior days, including today, to return. |
| `start` | date | no | Start date in YYYY-MM-DD format. |
| `end` | date | no | End date in YYYY-MM-DD format. |
| `bbox` | string | no | Bounding box as min lon, max lat, max lon, min lat. |
| `magId` | string | no | Filter by magnitude type ID. |
| `magMin` | number | no | Minimum magnitude value. |
| `magMax` | number | no | Maximum magnitude value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {
          "id": "string",
          "title": "string"
        }
      ],
      "closed": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "geometry": [
        {
          "coordinates": [
            1
          ],
          "date": "2026-05-07T12:00:00.000Z",
          "magnitudeUnit": "string",
          "magnitudeValue": 1,
          "type": "string"
        }
      ],
      "id": "string",
      "link": "https://example.com",
      "sources": [
        {
          "id": "string",
          "url": "https://example.com"
        }
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> |  |
| `categories[].id` | string |  |
| `categories[].title` | string |  |
| `closed` | date |  |
| `description` | string |  |
| `geometry` | array<object> |  |
| `geometry[].coordinates` | array<number> |  |
| `geometry[].date` | date |  |
| `geometry[].magnitudeUnit` | string |  |
| `geometry[].magnitudeValue` | number |  |
| `geometry[].type` | string |  |
| `id` | string |  |
| `link` | string |  |
| `sources` | array<object> |  |
| `sources[].id` | string |  |
| `sources[].url` | string |  |
| `title` | string |  |

## Native endpoint

Through the native EONET API, this operation is `GET /events` (base URL `https://eonet.gsfc.nasa.gov/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

