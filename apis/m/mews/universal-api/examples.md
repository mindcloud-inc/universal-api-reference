# Mews Universal API Examples

These examples use the MindCloud API key and Mews connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Configuration

Retrieves enterprise configuration from Mews.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-configuration?${params}`, {
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
      "enterprise": {},
      "isIdentityDocumentNumberRequired": true,
      "nowUtc": "2026-05-07T12:00:00.000Z",
      "paymentCardStorage": {},
      "service": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Configuration action reference](actions/get-configuration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mews/latest/actions/get-configuration).

## Add Task

Creates a new task in Mews.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mews/latest/actions/add-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "deadlineUtc": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mews/latest/actions/add-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "deadlineUtc": "2026-05-07T12:00:00.000Z"
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Task action reference](actions/add-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mews/latest/actions/add-task).
