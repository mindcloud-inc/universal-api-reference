# Needle Universal API Examples

These examples use the MindCloud API key and Needle connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get File Upload URL

Retrieves a signed file upload URL from Needle.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/needle/latest/actions/get-file-upload-url?connectionId=$CONNECTION_ID&contentType=application%2Fpdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contentType": "application/pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/needle/latest/actions/get-file-upload-url?${params}`, {
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
      "uploadUrl": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get File Upload URL action reference](actions/get-file-upload-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/needle/latest/actions/get-file-upload-url).

## Add Files To Collection

Adds files to a collection in Needle.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/needle/latest/actions/add-files-to-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "files[].name": "Ava Chen",
  "files[].url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/needle/latest/actions/add-files-to-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "files[].name": "Ava Chen",
    "files[].url": "https://example.com"
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
      "connectorId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "md5Hash": "string",
      "name": "Ava Chen",
      "size": 1,
      "status": "string",
      "type": "string",
      "url": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Files To Collection action reference](actions/add-files-to-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/needle/latest/actions/add-files-to-collection).
