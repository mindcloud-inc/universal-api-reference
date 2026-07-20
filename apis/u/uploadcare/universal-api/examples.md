# Uploadcare Universal API Examples

These examples use the MindCloud API key and Uploadcare connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Files

Retrieves all files from your Uploadcare project.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-files?${params}`, {
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
      "contentInfo": {},
      "datetimeRemoved": "2026-05-07T12:00:00.000Z",
      "datetimeStored": "2026-05-07T12:00:00.000Z",
      "datetimeUploaded": "2026-05-07T12:00:00.000Z",
      "isImage": true,
      "isReady": true,
      "metadata": {},
      "mimeType": "string",
      "originalFilename": "Ava Chen",
      "originalFileUrl": "https://example.com",
      "size": 1,
      "url": "https://example.com",
      "uuid": "string",
      "variations": {}
    }
  ],
  "meta": {}
}
```

See the full [List Files action reference](actions/list-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uploadcare/latest/actions/list-files).

## Batch Store Files

Stores multiple files in Uploadcare storage.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/batch-store-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/batch-store-files', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuids[]": ["string"]
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
      "problems": {},
      "result": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Batch Store Files action reference](actions/batch-store-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uploadcare/latest/actions/batch-store-files).
