# Prerender.io: List Aggregated Metrics Trial Overview

Retrieves a trial overview from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-trial-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-trial-overview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-trial-overview?${params}`, {
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
      "apiRequests": 1,
      "averageDeliveryTime": 1,
      "originalDeliveryTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiRequests` | number |  |
| `averageDeliveryTime` | number |  |
| `originalDeliveryTime` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/aggregated-metrics/trial-overview` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-aggregated-metrics-trial-overview.md) for the provider-specific parameters and requirements.

