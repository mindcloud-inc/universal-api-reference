# Finnish Railway Traffic: List compositions updated after version

Retrieves compositions updated after a version in Finnish Railway Traffic.

```
GET https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-compositions-updated-after-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish Railway Traffic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-compositions-updated-after-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-compositions-updated-after-version?${params}`, {
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
      "journeySections": [
        {}
      ],
      "operatorShortCode": "string",
      "operatorUICCode": 1,
      "trainCategory": "string",
      "trainNumber": 1,
      "trainType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departureDate` | date |  |
| `journeySections` | array<object> |  |
| `operatorShortCode` | string |  |
| `operatorUICCode` | number |  |
| `trainCategory` | string |  |
| `trainNumber` | number |  |
| `trainType` | string |  |

## Native endpoint

Through the native Finnish Railway Traffic API, this operation is `GET /api/v1/compositions` (base URL `https://rata.digitraffic.fi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-compositions-updated-after-version.md) for the provider-specific parameters and requirements.

