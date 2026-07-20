# EONET: List GeoJSON Event Features

Retrieves GeoJSON event features from EONET.

```
GET https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-geojson-event-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EONET `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-geojson-event-features?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-geojson-event-features?${params}`, {
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
      "geometry": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "properties": {
        "categories": [
          {
            "id": "string",
            "title": "string"
          }
        ],
        "closed": "2026-05-07T12:00:00.000Z",
        "date": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "id": "string",
        "link": "https://example.com",
        "magnitudeUnit": "string",
        "magnitudeValue": 1,
        "sources": [
          {
            "id": "string",
            "url": "https://example.com"
          }
        ],
        "title": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `geometry.coordinates` | array<number> |  |
| `geometry.type` | string |  |
| `properties.categories` | array<object> |  |
| `properties.categories[].id` | string |  |
| `properties.categories[].title` | string |  |
| `properties.closed` | date |  |
| `properties.date` | date |  |
| `properties.description` | string |  |
| `properties.id` | string |  |
| `properties.link` | string |  |
| `properties.magnitudeUnit` | string |  |
| `properties.magnitudeValue` | number |  |
| `properties.sources` | array<object> |  |
| `properties.sources[].id` | string |  |
| `properties.sources[].url` | string |  |
| `properties.title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native EONET API, this operation is `GET /events/geojson` (base URL `https://eonet.gsfc.nasa.gov/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-geojson-event-features.md) for the provider-specific parameters and requirements.

