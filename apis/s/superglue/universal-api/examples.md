# Superglue Universal API Examples

These examples use the MindCloud API key and Superglue connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tools

Retrieves tools from Superglue.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-tools?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-tools?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "inputSchema": {},
      "instruction": "string",
      "outputTransform": "string",
      "steps": [
        {}
      ],
      "systemIds": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Tools action reference](actions/list-tools.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/superglue/latest/actions/list-tools).

## Cancel Run

Cancels an existing run in Superglue.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/cancel-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "runId": "7f3e9c1a-2b4d-4e8f-9a3b-1c5d7e9f2a4b"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superglue/latest/actions/cancel-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "runId": "7f3e9c1a-2b4d-4e8f-9a3b-1c5d7e9f2a4b"
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
      "data": {},
      "error": "string",
      "executionMode": "string",
      "metadata": {
        "completedAt": "2026-05-07T12:00:00.000Z",
        "durationMs": 1,
        "startedAt": "2026-05-07T12:00:00.000Z"
      },
      "options": {},
      "requestSource": "string",
      "resultStorageUri": "string",
      "runId": "string",
      "status": "string",
      "stepResults": [
        {}
      ],
      "tool": {
        "id": "string",
        "instruction": "string",
        "name": "Ava Chen"
      },
      "toolId": "string",
      "toolPayload": {},
      "traceId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Run action reference](actions/cancel-run.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/superglue/latest/actions/cancel-run).
