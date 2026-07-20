# ChartLy: Create Multi-Series Chart (Zapier)

Creates a Zapier-friendly multi-series chart in Chartly.

```
POST https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/create-multi-series-chart-zapier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartLy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/create-multi-series-chart-zapier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "labels": "string",
  "series1_name": "Ava Chen",
  "series1_values": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/create-multi-series-chart-zapier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "labels": "string",
    "series1_name": "Ava Chen",
    "series1_values": "string"
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
| `chartType` | string | no | Chart type One of: `0`, `1`. Default: `bar`. |
| `series1_name` | string | yes | First series name |
| `series1_values` | string | yes | First series values (comma-separated) |
| `series1_color` | string | no | First series color Default: `#3B82F6`. |
| `series2_name` | string | no | Second series name |
| `series2_values` | string | no | Second series values (comma-separated) |
| `series2_color` | string | no | Second series color Default: `#10B981`. |
| `series3_name` | string | no | Third series name |
| `series3_values` | string | no | Third series values (comma-separated) |
| `series3_color` | string | no | Third series color Default: `#F59E0B`. |
| `width` | number | no | Chart width in pixels Default: `800`. |
| `height` | number | no | Chart height in pixels Default: `400`. |
| `format` | string | no | Output format One of: `0`, `1`. Default: `png`. |
| `backgroundColor` | string | no | Background color Default: `white`. |
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

Through the native ChartLy API, this operation is `POST /v1/zapier/multi-series-chart` (base URL `https://api.chartly.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multi-series-chart-zapier.md) for the provider-specific parameters and requirements.

