# Prembly: Geo-location

Creates a geolocation verification in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/geo-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/geo-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/geo-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "coordinates": {
        "latitude": 1,
        "longitude": 1
      },
      "geo_metadata": {
        "osm_class": "string",
        "osm_type": "string"
      },
      "matched_address": {
        "formatted_address": "string",
        "matched_level": "string",
        "matched_variant": "string"
      },
      "original_address": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coordinates.latitude` | number |  |
| `coordinates.longitude` | number |  |
| `geo_metadata.osm_class` | string |  |
| `geo_metadata.osm_type` | string |  |
| `matched_address.formatted_address` | string |  |
| `matched_address.matched_level` | string |  |
| `matched_address.matched_variant` | string |  |
| `original_address` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/address/geolocation/verification` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/geo-location.md) for the provider-specific parameters and requirements.

