# ThingsBoard Universal API Examples

These examples use the MindCloud API key and ThingsBoard connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from ThingsBoard.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-current-user?${params}`, {
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
      "authority": "string",
      "createdTime": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": {
        "entityType": "string",
        "id": "string"
      },
      "lastName": "Chen",
      "name": "Ava Chen",
      "phone": "string",
      "tenantId": {
        "entityType": "string",
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/thingsBoard/latest/actions/get-current-user).

## Acknowledge Alarm

Acknowledges an alarm in ThingsBoard.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/acknowledge-alarm" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alarmId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/acknowledge-alarm', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alarmId": "string"
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
      "ackTs": 1,
      "cleared": true,
      "createdTime": 1,
      "id": {
        "entityType": "string",
        "id": "string"
      },
      "originator": {
        "id": "string"
      },
      "severity": "string",
      "status": "string",
      "tenantId": {
        "id": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Acknowledge Alarm action reference](actions/acknowledge-alarm.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/thingsBoard/latest/actions/acknowledge-alarm).
