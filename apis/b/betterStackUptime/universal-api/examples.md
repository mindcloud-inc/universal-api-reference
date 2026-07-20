# Better Stack Uptime Universal API Examples

These examples use the MindCloud API key and Better Stack Uptime connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Heartbeat

Retrieves a heartbeat from Better Stack Uptime.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-heartbeat?connectionId=$CONNECTION_ID&heartbeatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "heartbeatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-heartbeat?${params}`, {
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

See the full [Get Heartbeat action reference](actions/get-heartbeat.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/betterStackUptime/latest/actions/get-heartbeat).

## Acknowledge Incident

Acknowledges an ongoing incident in Better Stack Uptime.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/acknowledge-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "incidentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/acknowledge-incident', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "incidentId": "string"
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

See the full [Acknowledge Incident action reference](actions/acknowledge-incident.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/betterStackUptime/latest/actions/acknowledge-incident).
