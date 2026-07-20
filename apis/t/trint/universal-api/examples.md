# Trint Universal API Examples

These examples use the MindCloud API key and Trint connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Files

Retrieves files from your Trint account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-files?${params}`, {
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
      "duration": 1,
      "excerpt": "string",
      "fileType": "string",
      "folderId": "string",
      "id": "string",
      "language": "string",
      "metadata": "string",
      "notes": "string",
      "timecode": "string",
      "timecodeOffsetEnabled": true,
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Files action reference](actions/list-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trint/latest/actions/list-files).

## Create Folder

Creates a new folder in Trint.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trint/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trint/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "_id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Folder action reference](actions/create-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trint/latest/actions/create-folder).
