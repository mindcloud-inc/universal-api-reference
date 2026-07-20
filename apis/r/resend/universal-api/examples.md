# Resend Universal API Examples

These examples use the MindCloud API key and Resend connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List API Keys

Retrieves API keys from Resend.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resend/latest/actions/list-api-keys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resend/latest/actions/list-api-keys?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastUsedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List API Keys action reference](actions/list-api-keys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/resend/latest/actions/list-api-keys).

## Cancel Email

Cancels a scheduled email in Resend.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/resend/latest/actions/cancel-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/resend/latest/actions/cancel-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Email action reference](actions/cancel-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/resend/latest/actions/cancel-email).
