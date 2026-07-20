# api.video: Retrieve aggregated metrics

Retrieves aggregated analytics metrics from api.video.

```
GET https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/retrieve-aggregated-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a api.video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/retrieve-aggregated-metrics?connectionId=$CONNECTION_ID&aggregation=string&metric=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aggregation": "string",
  "metric": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/retrieve-aggregated-metrics?${params}`, {
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
| `aggregation` | string | yes | The aggregation to apply to the metric. |
| `metric` | string | yes | The metric to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native api.video API returns.

## Native endpoint

Through the native api.video API, this operation is `GET /data/metrics/:metric/:aggregation` (base URL `https://ws.api.video`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-aggregated-metrics.md) for the provider-specific parameters and requirements.

