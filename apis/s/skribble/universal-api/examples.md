# Skribble Universal API Examples

These examples use the MindCloud API key and Skribble connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Signature Requests

Retrieves signature requests from Skribble.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/list-signature-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribble/latest/actions/list-signature-requests?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Signature Requests action reference](actions/list-signature-requests.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/skribble/latest/actions/list-signature-requests).

## Add Signature Request Attachment

Adds an attachment to a signature request in Skribble.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/add-signature-request-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "contentType": "string",
  "filename": "Ava Chen",
  "signatureRequestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skribble/latest/actions/add-signature-request-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "contentType": "string",
    "filename": "Ava Chen",
    "signatureRequestId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Signature Request Attachment action reference](actions/add-signature-request-attachment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/skribble/latest/actions/add-signature-request-attachment).
