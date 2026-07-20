# iLovePDFv2 Universal API Examples

These examples use the MindCloud API key and iLovePDFv2 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tasks



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/list-tasks?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "download_filename": "Ava Chen",
      "server": "string",
      "status": "string",
      "task": "string",
      "tool": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Tasks action reference](actions/list-tasks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iLovePDFv2/latest/actions/list-tasks).

## Connect Task

Creates a follow-up task from an iLovePDFv2 task.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/connect-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "server": "string",
  "task": "string",
  "tool": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/connect-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "server": "string",
    "task": "string",
    "tool": "string"
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
      "files": [
        {}
      ],
      "task": "string"
    }
  ],
  "meta": {}
}
```

See the full [Connect Task action reference](actions/connect-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iLovePDFv2/latest/actions/connect-task).
