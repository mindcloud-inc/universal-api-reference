# Cloro Universal API Examples

These examples use the MindCloud API key and Cloro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Countries



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloro/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloro/latest/actions/list-countries?${params}`, {
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
      "countryCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Countries action reference](actions/list-countries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloro/latest/actions/list-countries).

## Create Async Task



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloro/latest/actions/create-async-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskType": "string",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloro/latest/actions/create-async-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskType": "string",
    "payload": {}
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
      "credits": {
        "creditsCharged": 1,
        "creditsToCharge": 1
      },
      "success": true,
      "task": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "idempotencyKey": "string",
        "priority": 1,
        "status": "string",
        "taskType": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Async Task action reference](actions/create-async-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloro/latest/actions/create-async-task).
