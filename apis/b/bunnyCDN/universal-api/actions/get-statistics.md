# BunnyCDN: Get Statistics

Retrieves account usage statistics from BunnyCDN.

```
GET https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-statistics?${params}`, {
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
      "AverageOriginResponseTime": 1,
      "CacheHitRate": 1,
      "TotalBandwidthUsed": 1,
      "TotalOriginTraffic": 1,
      "TotalRequestsServed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AverageOriginResponseTime` | number |  |
| `CacheHitRate` | number |  |
| `TotalBandwidthUsed` | number |  |
| `TotalOriginTraffic` | number |  |
| `TotalRequestsServed` | number |  |

## Native endpoint

Through the native BunnyCDN API, this operation is `GET /statistics` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statistics.md) for the provider-specific parameters and requirements.

