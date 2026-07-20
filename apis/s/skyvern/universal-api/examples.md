# Skyvern Universal API Examples

These examples use the MindCloud API key and Skyvern connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Folders

Retrieves workflow folders for your organization from Skyvern.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-folders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-folders?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "folder_id": "string",
      "modified_at": "2026-05-07T12:00:00.000Z",
      "organization_id": "string",
      "title": "string",
      "workflow_count": 1
    }
  ],
  "meta": {}
}
```

See the full [List Folders action reference](actions/list-folders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/skyvern/latest/actions/list-folders).

## Cancel Run

Cancels a task or workflow run in Skyvern.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/cancel-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "runId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/cancel-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "runId": "string"
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

See the full [Cancel Run action reference](actions/cancel-run.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/skyvern/latest/actions/cancel-run).
