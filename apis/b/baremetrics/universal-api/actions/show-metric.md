# Baremetrics: Show Metric

Retrieves a metric from Baremetrics.

```
GET https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/show-metric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baremetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/show-metric?connectionId=$CONNECTION_ID&metric=mrr&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "metric": "mrr",
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/show-metric?${params}`, {
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
| `metric` | string | yes | You can see a list of available metrics [here](available-metrics) Example: `mrr`. |
| `startDate` | string | yes |  |
| `endDate` | string | yes |  |
| `compareTo` | number | no | The number of days ago to compare results to |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baremetrics API returns.

## Native endpoint

Through the native Baremetrics API, this operation is `GET /v1/metrics/:metric` (base URL `https://sandbox.baremetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-metric.md) for the provider-specific parameters and requirements.

