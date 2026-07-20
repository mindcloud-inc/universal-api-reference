# Finnish Railway Traffic: List stations

Retrieves stations from Finnish Railway Traffic.

```
GET https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-stations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish Railway Traffic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-stations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-stations?${params}`, {
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
      "countryCode": "string",
      "latitude": 1,
      "longitude": 1,
      "passengerTraffic": true,
      "stationName": "Ava Chen",
      "stationShortCode": "string",
      "stationType": "string",
      "stationUICCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryCode` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `passengerTraffic` | boolean |  |
| `stationName` | string |  |
| `stationShortCode` | string |  |
| `stationType` | string |  |
| `stationUICCode` | number |  |

## Native endpoint

Through the native Finnish Railway Traffic API, this operation is `GET /api/v1/metadata/stations` (base URL `https://rata.digitraffic.fi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stations.md) for the provider-specific parameters and requirements.

