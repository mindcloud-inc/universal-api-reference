# Clappia: Update Chart

Updates an existing chart in Clappia.

```
PUT https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-chart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-chart" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "chartIndex": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-chart', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "chartIndex": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clappia app ID. |
| `chartIndex` | number | yes | Zero-based chart index to update. |
| `chartTitle` | string | no | Updated display title for the chart. |
| `width` | number | no | Updated chart width percentage. |
| `isStacked` | boolean | no | Whether the updated chart should be stacked. |
| `direction` | string | no | Updated chart direction, such as Horizontal or Vertical. |
| `aggregationDimensions[]` | array<object> | no | Updated aggregation dimension objects for the chart metrics. |
| `dimensions[]` | array<object> | no | Updated dimension objects for the chart grouping axes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clappia API returns.

## Native endpoint

Through the native Clappia API, this operation is `POST /analytics/updateChart` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chart.md) for the provider-specific parameters and requirements.

