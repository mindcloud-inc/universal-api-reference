# Erase.bg Universal API Examples

These examples use the MindCloud API key and Erase.bg connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Files

Retrieves files from Erase.bg storage by search filters.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/list-files?${params}`, {
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
      "items": [
        {
          "_id": "string",
          "access": "string",
          "assetType": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "fileId": "string",
          "format": "string",
          "isActive": true,
          "name": "Ava Chen",
          "path": "string",
          "size": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com"
        }
      ],
      "page": {}
    }
  ],
  "meta": {}
}
```

See the full [List Files action reference](actions/list-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/erasebg/latest/actions/list-files).

## Create Folder

Creates a folder in Erase.bg storage.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/create-folder', {
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
      "isActive": true,
      "name": "Ava Chen",
      "path": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Folder action reference](actions/create-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/erasebg/latest/actions/create-folder).
