# EONET: List Events for Category

Retrieves events for a category from EONET.

```
GET https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-events-for-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EONET `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-events-for-category?connectionId=$CONNECTION_ID&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-events-for-category?${params}`, {
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
| `categoryId` | string | yes | Category ID such as wildfires or volcanoes. |
| `source` | string | no | Filter by source ID. Comma-separated values act as OR. |
| `status` | string | no | Filter events by status: open, closed, or all. |
| `days` | number | no | Return events from the last N days, including today. |
| `start` | date | no | Return events on or after this date (YYYY-MM-DD). |
| `end` | date | no | Return events on or before this date (YYYY-MM-DD). |

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

Through the native EONET API, this operation is `GET /categories/:categoryId` (base URL `https://eonet.gsfc.nasa.gov/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events-for-category.md) for the provider-specific parameters and requirements.

