# EONET: List GeoJSON Event Features for Event

Retrieves GeoJSON event features for an event from EONET.

```
GET https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-geojson-event-features-for-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EONET `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-geojson-event-features-for-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-geojson-event-features-for-event?${params}`, {
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
| `eventId` | string | yes | Unique EONET event ID. |

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
        "closed": "2026-05-07T12:00:00.000Z",
        "date": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "id": "string",
        "link": "https://example.com",
        "magnitudeUnit": "string",
        "magnitudeValue": 1,
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
| `properties.closed` | date |  |
| `properties.date` | date |  |
| `properties.description` | string |  |
| `properties.id` | string |  |
| `properties.link` | string |  |
| `properties.magnitudeUnit` | string |  |
| `properties.magnitudeValue` | number |  |
| `properties.title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native EONET API, this operation is `GET /events/:eventId/geojson` (base URL `https://eonet.gsfc.nasa.gov/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-geojson-event-features-for-event.md) for the provider-specific parameters and requirements.

