# LogMeIn Universal API Examples

These examples use the MindCloud API key and LogMeIn connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Settings

Retrieves knowledge base user settings from LogMeIn.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-user-settings?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "timezone": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Settings action reference](actions/get-user-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logMeIn/latest/actions/get-user-settings).

## Acknowledge Alerts

Updates alerts by acknowledging them in LogMeIn.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/acknowledge-alerts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "acknowledgeData[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/acknowledge-alerts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "acknowledgeData[]": [{}]
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
      "acknowledged": true,
      "alertId": "string",
      "deviceId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Acknowledge Alerts action reference](actions/acknowledge-alerts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logMeIn/latest/actions/acknowledge-alerts).
