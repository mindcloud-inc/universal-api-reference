# ChartLy Universal API Examples

These examples use the MindCloud API key and ChartLy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Status

Retrieves Chartly API health and configuration status.

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

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Get Status action reference](actions/get-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chartLy/latest/actions/get-status).

## Create Bar Chart (Zapier)

Creates a Zapier-friendly bar chart in Chartly.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/create-bar-chart-zapier" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/create-bar-chart-zapier', {
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

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Bar Chart (Zapier) action reference](actions/create-bar-chart-zapier.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chartLy/latest/actions/create-bar-chart-zapier).
