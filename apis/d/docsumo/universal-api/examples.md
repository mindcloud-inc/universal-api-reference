# Docsumo Universal API Examples

These examples use the MindCloud API key and Docsumo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User And Document Types

Retrieves your Docsumo user details and active document types.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/get-user-and-document-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/get-user-and-document-types?${params}`, {
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
      "data": {},
      "error": "string",
      "error_code": "string",
      "message": "string",
      "source": "string",
      "status": "string",
      "status_code": 1
    }
  ],
  "meta": {}
}
```

See the full [Get User And Document Types action reference](actions/get-user-and-document-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docsumo/latest/actions/get-user-and-document-types).

## Add Files In Folder

Uploads a document into a specific Docsumo folder.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/add-files-in-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "folder_id": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/add-files-in-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "folder_id": "string",
    "type": "string"
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
      "error_code": "string",
      "message": "string",
      "source": "string",
      "status": "string",
      "status_code": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Files In Folder action reference](actions/add-files-in-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docsumo/latest/actions/add-files-in-folder).
