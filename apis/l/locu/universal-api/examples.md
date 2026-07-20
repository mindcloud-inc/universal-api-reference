# Locu Universal API Examples

These examples use the MindCloud API key and Locu connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the authenticated user and workspace from Locu.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-current-user?${params}`, {
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
      "workspaceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/locu/latest/actions/get-current-user).

## Continue Timer

Updates the Locu timer by resuming it.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/locu/latest/actions/continue-timer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/locu/latest/actions/continue-timer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "currentTaskId": "string",
      "duration": 1,
      "startedAt": "2026-05-07T12:00:00.000Z",
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [Continue Timer action reference](actions/continue-timer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/locu/latest/actions/continue-timer).
