# File.io Universal API Examples

These examples use the MindCloud API key and File.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Files

Retrieves files from File.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileio/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileio/latest/actions/list-files?${params}`, {
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
      "autoDelete": true,
      "created": "2026-05-07T12:00:00.000Z",
      "downloads": 1,
      "expires": "2026-05-07T12:00:00.000Z",
      "expiry": "string",
      "id": "string",
      "key": "string",
      "link": "https://example.com",
      "maxDownloads": 1,
      "mimeType": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

See the full [List Files action reference](actions/list-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fileio/latest/actions/list-files).

## Replace File

Updates a file in File.io, resetting omitted fields.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fileio/latest/actions/replace-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fileio/latest/actions/replace-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string"
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
      "autoDelete": true,
      "created": "2026-05-07T12:00:00.000Z",
      "downloads": 1,
      "expires": "2026-05-07T12:00:00.000Z",
      "expiry": "string",
      "id": "string",
      "key": "string",
      "link": "https://example.com",
      "maxDownloads": 1,
      "mimeType": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "size": 1,
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Replace File action reference](actions/replace-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fileio/latest/actions/replace-file).
