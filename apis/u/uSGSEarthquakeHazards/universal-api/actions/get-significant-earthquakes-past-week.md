# USGS Earthquake Hazards: Get Significant Earthquakes Past Week

Retrieves significant earthquakes from the past week.

```
GET https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-significant-earthquakes-past-week
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USGS Earthquake Hazards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-significant-earthquakes-past-week?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-significant-earthquakes-past-week?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "features": [
        {
          "geometry": {
            "coordinates": [
              1
            ]
          },
          "id": "string",
          "properties": {
            "mag": 1,
            "place": "string",
            "time": 1,
            "title": "string"
          }
        }
      ],
      "metadata": {
        "count": 1,
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
| `features` | array<object> |  |
| `features[].geometry.coordinates` | array<number> |  |
| `features[].id` | string |  |
| `features[].properties.mag` | number |  |
| `features[].properties.place` | string |  |
| `features[].properties.time` | number |  |
| `features[].properties.title` | string |  |
| `metadata` | object |  |
| `metadata.count` | number |  |
| `metadata.title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native USGS Earthquake Hazards API, this operation is `GET /earthquakes/feed/v1.0/summary/significant_week.geojson` (base URL `https://earthquake.usgs.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-significant-earthquakes-past-week.md) for the provider-specific parameters and requirements.

