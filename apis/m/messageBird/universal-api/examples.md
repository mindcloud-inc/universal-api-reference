# MessageBird Universal API Examples

These examples use the MindCloud API key and MessageBird connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspace Channels



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/list-workspace-channels?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/list-workspace-channels?${params}`, {
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
      "nextPageToken": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Workspace Channels action reference](actions/list-workspace-channels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/messageBird/latest/actions/list-workspace-channels).

## Add Allow/Block Rules in Bulk



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/add-allowblock-rules-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/add-allowblock-rules-in-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string"
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
      "bulkId": "string",
      "currentIndex": 1,
      "errors": [
        "string"
      ],
      "status": "string",
      "total": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Allow/Block Rules in Bulk action reference](actions/add-allowblock-rules-in-bulk.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/messageBird/latest/actions/add-allowblock-rules-in-bulk).
