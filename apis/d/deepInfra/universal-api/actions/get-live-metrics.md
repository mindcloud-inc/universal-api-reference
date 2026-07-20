# Deep Infra: Get Live Metrics



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-live-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-live-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-live-metrics?${params}`, {
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
      "requestsPerSecond": 1,
      "timeToFirstToken": 1,
      "tokensPerSecond": 1,
      "totalTflops": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestsPerSecond` | number | Current requests served per second. |
| `timeToFirstToken` | number | Current average time to first token. |
| `tokensPerSecond` | number | Current tokens served per second. |
| `totalTflops` | number | Current total TFLOPS reported by DeepInfra. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/metrics/live` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-live-metrics.md) for the provider-specific parameters and requirements.

