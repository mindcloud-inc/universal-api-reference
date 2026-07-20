# Wrike Universal API Examples

These examples use the MindCloud API key and Wrike connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tasks

Finds tasks in Wrike.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-tasks?${params}`, {
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
      "accountId": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "customStatusId": "string",
      "dates": {},
      "entityTypeId": "string",
      "id": "string",
      "importance": "string",
      "permalink": "https://example.com",
      "priority": "string",
      "scope": "string",
      "status": "string",
      "title": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Tasks action reference](actions/list-tasks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wrike/latest/actions/list-tasks).

## Create Folder

Creates a new folder in a Wrike folder.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wrike/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "string",
    "title": "string"
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
      "childIds": [
        "string"
      ],
      "color": "string",
      "customItemTypeId": "string",
      "id": "string",
      "project": {},
      "scope": "string",
      "space": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Folder action reference](actions/create-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wrike/latest/actions/create-folder).
