# ChartLy: Get Status

Retrieves Chartly API health and configuration status.

```
GET https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/get-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartLy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/get-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ChartLy API returns.

## Native endpoint

Through the native ChartLy API, this operation is `GET /v1/status` (base URL `https://api.chartly.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-status.md) for the provider-specific parameters and requirements.

