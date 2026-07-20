# USGS Earthquake Hazards: Get Earthquake By Event ID

Finds an earthquake in USGS Earthquake Hazards by event ID.

```
GET https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-earthquake-by-event-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USGS Earthquake Hazards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-earthquake-by-event-id?connectionId=$CONNECTION_ID&eventid=us7000pn9s" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventid": "us7000pn9s"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-earthquake-by-event-id?${params}`, {
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
| `eventid` | string | yes | USGS event identifier to retrieve. Example: `us7000pn9s`. |

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
      "id": "string",
      "properties": {
        "detail": "string",
        "mag": 1,
        "place": "string",
        "status": "string",
        "time": "2026-05-07T12:00:00.000Z",
        "title": "string",
        "tsunami": 1,
        "type": "string",
        "updated": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com"
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
| `geometry` | object | GeoJSON point geometry. |
| `geometry.coordinates` | array<number> | Longitude, latitude, and depth coordinates. |
| `geometry.type` | string | GeoJSON geometry type. |
| `id` | string | USGS event identifier. |
| `properties` | object | Earthquake event properties. |
| `properties.detail` | string | USGS detail feed URL for the event. |
| `properties.mag` | number | Earthquake magnitude. |
| `properties.place` | string | Event location description. |
| `properties.status` | string | Event review status. |
| `properties.time` | date | Event origin time. |
| `properties.title` | string | Human-readable event title. |
| `properties.tsunami` | number | Tsunami flag reported by USGS. |
| `properties.type` | string | Event type. |
| `properties.updated` | date | Last update time for the event. |
| `properties.url` | string | USGS event detail URL. |
| `type` | string | GeoJSON object type for the returned earthquake feature. |

## Native endpoint

Through the native USGS Earthquake Hazards API, this operation is `GET /fdsnws/event/1/query` (base URL `https://earthquake.usgs.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-earthquake-by-event-id.md) for the provider-specific parameters and requirements.

