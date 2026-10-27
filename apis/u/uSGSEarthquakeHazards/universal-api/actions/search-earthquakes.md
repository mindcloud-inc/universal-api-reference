# USGS Earthquake Hazards: Search Earthquakes

Finds earthquakes in USGS Earthquake Hazards by search parameters.

```
GET https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/search-earthquakes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USGS Earthquake Hazards `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/search-earthquakes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/search-earthquakes?${params}`, {
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
| `starttime` | string | no | Only return events on or after this ISO8601 UTC time. Example: `2026-05-01T00:00:00Z`. |
| `endtime` | string | no | Only return events on or before this ISO8601 UTC time. Example: `2026-05-04T00:00:00Z`. |
| `minmagnitude` | number | no | Only return events with magnitude greater than or equal to this value. Example: `2.5`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maxmagnitude` | number | no | Only return events with magnitude less than or equal to this value. Example: `6`. |
| `latitude` | number | no | Latitude for radius search. Use with longitude and maximum radius in kilometers. Example: `37.7749`. |
| `longitude` | number | no | Longitude for radius search. Use with latitude and maximum radius in kilometers. Example: `-122.4194`. |
| `maxradiuskm` | number | no | Maximum distance in kilometers from the latitude and longitude point. Example: `100`. |
| `eventtype` | string | no | Limit results to a USGS event type such as earthquake. Default: `earthquake`. |
| `orderby` | string | no | USGS event ordering mode. One of: `0`, `1`, `2`, `3`. Default: `time`. |
| `limit` | number | no | Maximum number of events to return. Default: `5`. |
| `offset` | number | no | One-based result offset for USGS catalog pagination. Default: `1`. |

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
        "time": 1,
        "title": "string",
        "type": "string",
        "updated": 1,
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
| `properties.detail` | string | USGS detail feed URL. |
| `properties.mag` | number | Event magnitude. |
| `properties.place` | string | Event place description. |
| `properties.status` | string | Event review status. |
| `properties.time` | number | Event time in milliseconds. |
| `properties.title` | string | Human-readable event title. |
| `properties.type` | string | USGS event type. |
| `properties.updated` | number | Last update time in milliseconds. |
| `properties.url` | string | USGS event page URL. |
| `type` | string | GeoJSON object type. |

## Native endpoint

Through the native USGS Earthquake Hazards API, this operation is `GET /fdsnws/event/1/query` (base URL `https://earthquake.usgs.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-earthquakes.md) for the provider-specific parameters and requirements.

