# Clappia: Add Chart

Creates a new chart in Clappia.

```
POST https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-chart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-chart" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "chartIndex": 1,
  "chartType": "string",
  "aggregationDimensions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-chart', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "chartIndex": 1,
    "chartType": "string",
    "aggregationDimensions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clappia app ID. |
| `chartIndex` | number | yes | Zero-based chart index where the new chart should be inserted. |
| `chartType` | string | yes | Chart type, such as barGraph. |
| `chartTitle` | string | no | Display title for the chart. |
| `width` | number | no | Chart width percentage. |
| `isStacked` | boolean | no | Whether the chart should be stacked. |
| `direction` | string | no | Chart direction, such as Horizontal or Vertical. |
| `aggregationDimensions[]` | array<object> | yes | Aggregation dimension objects that define the chart metrics. |
| `dimensions[]` | array<object> | no | Dimension objects that define the chart grouping axes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clappia API returns.

## Native endpoint

Through the native Clappia API, this operation is `POST /analytics/addChart` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-chart.md) for the provider-specific parameters and requirements.

