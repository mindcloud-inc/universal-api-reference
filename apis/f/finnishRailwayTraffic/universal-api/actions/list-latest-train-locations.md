# Finnish Railway Traffic: List latest train locations

Retrieves latest train locations from Finnish Railway Traffic.

```
GET https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-latest-train-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish Railway Traffic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-latest-train-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-latest-train-locations?${params}`, {
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
      "departureDate": "2026-05-07T12:00:00.000Z",
      "location": {},
      "speed": 1,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "trainNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departureDate` | date |  |
| `location` | object |  |
| `speed` | number |  |
| `timestamp` | date |  |
| `trainNumber` | number |  |

## Native endpoint

Through the native Finnish Railway Traffic API, this operation is `GET /api/v1/train-locations/latest` (base URL `https://rata.digitraffic.fi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-latest-train-locations.md) for the provider-specific parameters and requirements.

