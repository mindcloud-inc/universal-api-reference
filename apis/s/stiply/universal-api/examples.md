# Stiply Universal API Examples

These examples use the MindCloud API key and Stiply connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sign Requests

Retrieves sign requests available in Stiply.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-sign-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-sign-requests?${params}`, {
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
      "allSignedAt": "string",
      "callBackUrl": "https://example.com",
      "canceledAt": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "string",
      "externalKey": "string",
      "id": 1,
      "key": "string",
      "rejectedAt": "string",
      "sentAt": "string",
      "signingSequenceType": "string",
      "signingType": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Sign Requests action reference](actions/list-sign-requests.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stiply/latest/actions/list-sign-requests).

## Cancel Sign Request

Cancels an existing Stiply sign request.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/cancel-sign-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signRequest": 1,
  "notifySigners": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stiply/latest/actions/cancel-sign-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signRequest": 1,
    "notifySigners": true
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

See the full [Cancel Sign Request action reference](actions/cancel-sign-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stiply/latest/actions/cancel-sign-request).
