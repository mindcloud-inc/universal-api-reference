# Lumin Universal API Examples

These examples use the MindCloud API key and Lumin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Information



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-user-information?${params}`, {
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
      "user": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get User Information action reference](actions/get-user-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lumin/latest/actions/get-user-information).

## Create Document



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentName": "Ava Chen",
  "fileUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lumin/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentName": "Ava Chen",
    "fileUrl": "https://example.com"
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
      "document": {
        "createdAt": 1,
        "id": "string",
        "location": {
          "folderId": "string",
          "spaceId": "string",
          "type": "string",
          "workspaceId": "string"
        },
        "mimeType": "string",
        "name": "Ava Chen",
        "previewUrl": "https://example.com",
        "size": 1,
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Document action reference](actions/create-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lumin/latest/actions/create-document).
