# ChartLy: Create Line Chart (Zapier)

Creates a Zapier-friendly line chart in Chartly.

```
POST https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/create-line-chart-zapier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartLy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/create-line-chart-zapier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "labels": "string",
  "values": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/create-line-chart-zapier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "labels": "string",
    "values": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Chart title |
| `labels` | string | yes | Comma-separated labels |
| `values` | string | yes | Comma-separated numeric values |
| `color` | string | no | Line color in hex Default: `#10B981`. |
| `width` | number | no | Chart width in pixels Default: `800`. |
| `height` | number | no | Chart height in pixels Default: `400`. |
| `format` | string | no | Output format One of: `0`, `1`. Default: `png`. |
| `backgroundColor` | string | no | Background color Default: `white`. |
| `fillArea` | boolean | no | Fill area under the line Default: `false`. |
| `showPoints` | boolean | no | Show data points Default: `true`. |
| `tension` | number | no | Line curve tension from 0 to 1 Default: `0.4`. |
| `showLegend` | boolean | no | Show legend Default: `true`. |
| `showGrid` | boolean | no | Show grid lines Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chartId": "string",
      "chartUrl": "https://example.com",
      "downloadUrl": "https://example.com",
      "format": "string",
      "height": 1,
      "previewUrl": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chartId` | string | Chart ID |
| `chartUrl` | string | Permanent chart URL |
| `downloadUrl` | string | Direct download URL |
| `format` | string | Chart format |
| `height` | number | Chart height |
| `previewUrl` | string | Preview URL |
| `width` | number | Chart width |

## Native endpoint

Through the native ChartLy API, this operation is `POST /v1/zapier/line-chart` (base URL `https://api.chartly.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-line-chart-zapier.md) for the provider-specific parameters and requirements.

