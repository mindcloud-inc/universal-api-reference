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
      "bbox": [
        1
      ],
      "features": [
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
            "updated": 1,
            "url": "https://example.com"
          }
        }
      ],
      "metadata": {
        "count": 1,
        "generated": 1,
        "status": 1,
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
| `bbox` | array<number> | Bounding box for returned event features. |
| `features` | array<object> | Earthquake event GeoJSON features. |
| `features[].geometry.coordinates` | array<number> | Longitude, latitude, and depth coordinates. |
| `features[].geometry.type` | string | GeoJSON geometry type. |
| `features[].id` | string | USGS event identifier. |
| `features[].properties.detail` | string | USGS detail feed URL. |
| `features[].properties.mag` | number | Event magnitude. |
| `features[].properties.place` | string | Event place description. |
| `features[].properties.status` | string | Event review status. |
| `features[].properties.time` | number | Event time in milliseconds. |
| `features[].properties.title` | string | Human-readable event title. |
| `features[].properties.updated` | number | Last update time in milliseconds. |
| `features[].properties.url` | string | USGS event page URL. |
| `metadata` | object | USGS feed metadata including generated time, URL, title, status, API version, and count. |
| `metadata.count` | number | Number of returned features. |
| `metadata.generated` | number | Generation timestamp in milliseconds. |
| `metadata.status` | number | HTTP-like status code. |
| `metadata.title` | string | USGS result title. |
| `type` | string | GeoJSON object type. |

## Native endpoint

Through the native USGS Earthquake Hazards API, this operation is `GET /fdsnws/event/1/query` (base URL `https://earthquake.usgs.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-earthquakes.md) for the provider-specific parameters and requirements.

