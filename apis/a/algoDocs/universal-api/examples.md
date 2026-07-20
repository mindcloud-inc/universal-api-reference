# AlgoDocs Universal API Examples

These examples use the MindCloud API key and AlgoDocs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current AlgoDocs user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/get-current-user?${params}`, {
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
      "email": "ava@example.com",
      "fullName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/algoDocs/latest/actions/get-current-user).

## Upload Document From Local Path

Creates a document in AlgoDocs from a local file.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/upload-document-from-local-path" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "extractorId": "string",
  "folderId": "string",
  "file": "/path/to/document.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/upload-document-from-local-path', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "extractorId": "string",
    "folderId": "string",
    "file": "/path/to/document.pdf"
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
      "fileMD5CheckSum": "string",
      "fileSize": 1,
      "id": 1,
      "uploadedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Upload Document From Local Path action reference](actions/upload-document-from-local-path.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/algoDocs/latest/actions/upload-document-from-local-path).
