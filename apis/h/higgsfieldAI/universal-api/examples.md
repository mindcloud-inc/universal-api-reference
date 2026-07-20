# Higgsfield AI Universal API Examples

These examples use the MindCloud API key and Higgsfield AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Request Status

Retrieves a generation request status from Higgsfield AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/get-request-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/get-request-status?${params}`, {
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
      "cancel_url": "https://example.com",
      "error": "string",
      "images": [
        {}
      ],
      "request_id": "string",
      "status": "string",
      "status_url": "https://example.com",
      "video": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Request Status action reference](actions/get-request-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/higgsfieldAI/latest/actions/get-request-status).

## Cancel Pending Request

Cancels a pending generation request in Higgsfield AI.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/cancel-pending-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/cancel-pending-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestId": "string"
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
      "error": "string",
      "request_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Pending Request action reference](actions/cancel-pending-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/higgsfieldAI/latest/actions/cancel-pending-request).
