# ConvertHub Universal API Examples

These examples use the MindCloud API key and ConvertHub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details

Retrieves account credits and plan details from ConvertHub.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-account-details?${params}`, {
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
      "credits_remaining": 1,
      "plan": {
        "credits": 1,
        "file_size_limit": 1,
        "file_size_limit_mb": 1,
        "name": "Ava Chen",
        "price": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/convertHub/latest/actions/get-account-details).

## Complete Chunked Upload

Completes a chunked upload and starts conversion in ConvertHub.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/complete-chunked-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "upload_987f6543-a21b-98c7-d654-321098765432"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/complete-chunked-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "upload_987f6543-a21b-98c7-d654-321098765432"
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
      "job_id": "string",
      "links": {
        "cancel": "https://example.com",
        "status": "https://example.com"
      },
      "message": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Complete Chunked Upload action reference](actions/complete-chunked-upload.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/convertHub/latest/actions/complete-chunked-upload).
