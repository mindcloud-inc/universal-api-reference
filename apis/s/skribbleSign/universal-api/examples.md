# Skribble Sign Universal API Examples

These examples use the MindCloud API key and Skribble Sign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get System Health

Retrieves system health from Skribble Sign.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-system-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-system-health?${params}`, {
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
      "groups": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get System Health action reference](actions/get-system-health.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/skribbleSign/latest/actions/get-system-health).

## Add Signature Request Attachment

Adds an attachment to a signature request in Skribble Sign.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/add-signature-request-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string",
  "filename": "Ava Chen",
  "contentType": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/add-signature-request-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureRequestId": "string",
    "filename": "Ava Chen",
    "contentType": "string",
    "content": "string"
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
      "content_type": "string",
      "filename": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Signature Request Attachment action reference](actions/add-signature-request-attachment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/skribbleSign/latest/actions/add-signature-request-attachment).
