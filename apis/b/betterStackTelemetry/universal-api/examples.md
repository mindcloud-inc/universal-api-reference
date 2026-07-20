# Better Stack Telemetry Universal API Examples

These examples use the MindCloud API key and Better Stack Telemetry connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Export Dashboard

Exports a dashboard from Better Stack Telemetry.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/export-dashboard?connectionId=$CONNECTION_ID&id=164807" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "164807"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/export-dashboard?${params}`, {
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

See the full [Export Dashboard action reference](actions/export-dashboard.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/betterStackTelemetry/latest/actions/export-dashboard).

## Create Exploration Alert

Creates a new exploration alert in Better Stack Telemetry.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/create-exploration-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "explorationId": "746510",
  "name": "mc-stage3-alert-paused",
  "alertType": "threshold",
  "confirmationPeriod": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/create-exploration-alert', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "explorationId": "746510",
    "name": "mc-stage3-alert-paused",
    "alertType": "threshold",
    "confirmationPeriod": "0"
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

See the full [Create Exploration Alert action reference](actions/create-exploration-alert.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/betterStackTelemetry/latest/actions/create-exploration-alert).
