# Onfleet Universal API Examples

These examples use the MindCloud API key and Onfleet connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test API Key

Tests an Onfleet API key for validity.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/test-api-key?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test API Key action reference](actions/test-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onfleet/latest/actions/test-api-key).

## Auto-Assign Tasks

Assigns tasks to workers automatically in Onfleet.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/auto-assign-tasks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tasks[]": [
    "string"
  ],
  "options.mode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/auto-assign-tasks', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tasks[]": ["string"],
    "options.mode": "string"
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
      "assignedTasks": {},
      "assignedTasksCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Auto-Assign Tasks action reference](actions/auto-assign-tasks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onfleet/latest/actions/auto-assign-tasks).
