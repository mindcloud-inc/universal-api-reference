# UptimeRobot Universal API Examples

These examples use the MindCloud API key and UptimeRobot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details

Retrieves account details and monitor counts from UptimeRobot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/get-account-details?${params}`, {
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
      "account": {},
      "stat": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uptimeRobot/latest/actions/get-account-details).

## Create Maintenance Window

Creates a new maintenance window in UptimeRobot.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/create-maintenance-window" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "friendly_name": "Ava Chen",
  "type": 1,
  "start_time": "string",
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/create-maintenance-window', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "friendly_name": "Ava Chen",
    "type": 1,
    "start_time": "string",
    "duration": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "mwindow": {},
      "stat": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Maintenance Window action reference](actions/create-maintenance-window.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uptimeRobot/latest/actions/create-maintenance-window).
