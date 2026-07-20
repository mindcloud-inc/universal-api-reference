# IQAir AirVisual: List Stations



```
GET https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-stations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IQAir AirVisual `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-stations?connectionId=$CONNECTION_ID&city=Beijing&state=Beijing&country=China" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "city": "Beijing",
  "state": "Beijing",
  "country": "China"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-stations?${params}`, {
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
| `city` | string | yes | City name exactly as returned by the List Cities action. Example: `Beijing`. |
| `state` | string | yes | State name exactly as returned by the List States action. Example: `Beijing`. |
| `country` | string | yes | Country name exactly as returned by the List Countries action. Example: `China`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "location": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "station": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `location` | object | Geospatial location payload for the station. |
| `location.coordinates` | array<number> | Longitude and latitude coordinates in GeoJSON order. |
| `location.type` | string | GeoJSON geometry type. |
| `station` | string | Station display name. |

## Native endpoint

Through the native IQAir AirVisual API, this operation is `GET /v2/stations` (base URL `https://api.airvisual.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stations.md) for the provider-specific parameters and requirements.

