# Image-Charts Universal API Examples

These examples use the MindCloud API key and Image-Charts connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Create Base64-Encoded Chart.js Image Chart

Creates a Base64-encoded Chart.js image chart with Image-Charts.

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

Example response:

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

See the full [Create Base64-Encoded Chart.js Image Chart action reference](actions/create-base64-encoded-chart-js-image-chart.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/imageCharts/latest/actions/create-base64-encoded-chart-js-image-chart).
