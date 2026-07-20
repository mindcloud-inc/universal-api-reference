# Files.com Universal API Examples

These examples use the MindCloud API key and Files.com connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Site

Retrieves current site settings from Files.com.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-site?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "dav_enabled": true,
      "email": "ava@example.com",
      "ftp_enabled": true,
      "id": 1,
      "name": "Ava Chen",
      "sftp_enabled": true,
      "sharing_enabled": true,
      "ssl_required": true,
      "subdomain": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Site action reference](actions/get-site.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/filescom/latest/actions/get-site).

## Begin File Upload

Begins a file upload in Files.com.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/begin-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "string",
  "size": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filescom/latest/actions/begin-file-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "path": "string",
    "size": 1
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
      "action": "string",
      "available_parts": 1,
      "expires": "2026-05-07T12:00:00.000Z",
      "headers": {},
      "http_method": "string",
      "next_partsize": 1,
      "parallel_parts": true,
      "parameters": {},
      "part_number": 1,
      "partsize": 1,
      "ref": "string",
      "retry_parts": true,
      "send": {},
      "upload_uri": "string"
    }
  ],
  "meta": {}
}
```

See the full [Begin File Upload action reference](actions/begin-file-upload.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/filescom/latest/actions/begin-file-upload).
