# Image-Charts: Create Base64-Encoded Chart.js Image Chart

Creates a Base64-encoded Chart.js image chart with Image-Charts.

```
GET https://connect.mindcloud.co/v1/universal/imageCharts/latest/actions/create-base64-encoded-chart-js-image-chart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Image-Charts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageCharts/latest/actions/create-base64-encoded-chart-js-image-chart?connectionId=$CONNECTION_ID&chart=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chart": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageCharts/latest/actions/create-base64-encoded-chart-js-image-chart?${params}`, {
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
| `chart` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Binary image bytes returned by Image-Charts. |
| `type` | string | Node.js buffer type label from the raw binary response wrapper. |

## Native endpoint

Through the native Image-Charts API, this operation is `GET /chart.js/2.8.0` (base URL `https://image-charts.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-base64-encoded-chart-js-image-chart.md) for the provider-specific parameters and requirements.

