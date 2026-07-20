# PiAPI/DiffRhythm Universal API Examples

These examples use the MindCloud API key and PiAPI/DiffRhythm connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## PiAPI Account Info

Retrieves your account information from PiAPI/DiffRhythm.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/piapi-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/piapi-account-info?${params}`, {
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
      "credit_pack_info": {
        "available_credits": 1
      },
      "equivalent_in_usd": 1,
      "id": 1,
      "max_concurrent_task_count": 1,
      "name": "Ava Chen",
      "plan": "string",
      "type": "string",
      "wallet": {
        "llm_remain": 1,
        "llm_used": 1,
        "point_remain": 1,
        "point_used": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [PiAPI Account Info action reference](actions/piapi-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIDiffRhythm/latest/actions/piapi-account-info).

## File Upload API

Creates a temporary file upload in PiAPI/DiffRhythm.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/file-upload-api" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen",
  "fileData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/file-upload-api', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen",
    "fileData": "string"
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
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [File Upload API action reference](actions/file-upload-api.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIDiffRhythm/latest/actions/file-upload-api).
