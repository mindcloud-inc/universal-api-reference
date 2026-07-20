# ChartLy: Render Chart From JSON

Renders a chart image from JSON config in Chartly.

```
POST https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/render-chart-from-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartLy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/render-chart-from-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chart": "string",
  "width": 1,
  "height": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/render-chart-from-json', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chart": "string",
    "width": 1,
    "height": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chart` | string | yes | Chart.js config as JSON string |
| `width` | number | yes | Image width in pixels |
| `height` | number | yes | Image height in pixels |
| `format` | string | no | Output format One of: `0`, `1`. Default: `png`. |
| `backgroundColor` | string | no | CSS background color |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ChartLy API returns.

## Native endpoint

Through the native ChartLy API, this operation is `POST /v1/chart` (base URL `https://api.chartly.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-chart-from-json.md) for the provider-specific parameters and requirements.

