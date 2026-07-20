# HyperDone Universal API Examples

These examples use the MindCloud API key and HyperDone connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Board Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperDone/latest/actions/get-board-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperDone/latest/actions/get-board-info?${params}`, {
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
      "boardGuid": "string",
      "boardName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Board Info action reference](actions/get-board-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hyperDone/latest/actions/get-board-info).

## Create Task



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperDone/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskName": "Weekly planning task"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperDone/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskName": "Weekly planning task"
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

See the full [Create Task action reference](actions/create-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hyperDone/latest/actions/create-task).
