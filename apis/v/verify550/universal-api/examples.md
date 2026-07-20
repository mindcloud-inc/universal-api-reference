# Verify550 Universal API Examples

These examples use the MindCloud API key and Verify550 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Single Email

Verifies a single email address with Verify550.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verify550/latest/actions/verify-single-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verify550/latest/actions/verify-single-email?${params}`, {
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
      "message": "string",
      "result": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Verify Single Email action reference](actions/verify-single-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verify550/latest/actions/verify-single-email).

## Upload Bulk Email File

Uploads a bulk email file to Verify550.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/verify550/latest/actions/upload-bulk-email-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "file_contents": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verify550/latest/actions/upload-bulk-email-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "file_contents": "string"
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
      "filename": "Ava Chen",
      "id": 1,
      "jobId": 1,
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Upload Bulk Email File action reference](actions/upload-bulk-email-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verify550/latest/actions/upload-bulk-email-file).
