# Finnish Railway Traffic: List routesets updated after version

Retrieves routesets updated after a version in Finnish Railway Traffic.

```
GET https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-routesets-updated-after-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish Railway Traffic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-routesets-updated-after-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-routesets-updated-after-version?${params}`, {
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
      "id": 1,
      "messageDateTime": "2026-05-07T12:00:00.000Z",
      "routes": [
        {}
      ],
      "trainNumber": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departureDate` | date |  |
| `id` | number |  |
| `messageDateTime` | date |  |
| `routes` | array<object> |  |
| `trainNumber` | number |  |
| `version` | number |  |

## Native endpoint

Through the native Finnish Railway Traffic API, this operation is `GET /api/v1/routesets` (base URL `https://rata.digitraffic.fi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-routesets-updated-after-version.md) for the provider-specific parameters and requirements.

