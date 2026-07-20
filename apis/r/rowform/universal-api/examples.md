# Rowform Universal API Examples

These examples use the MindCloud API key and Rowform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Authentication

Retrieves API key validation details from Rowform.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rowform/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rowform/latest/actions/test-authentication?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "key_name": "Ava Chen",
      "name": "Ava Chen",
      "scopes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Test Authentication action reference](actions/test-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rowform/latest/actions/test-authentication).

## Subscribe Webhook

Creates a webhook subscription in Rowform.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rowform/latest/actions/subscribe-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hookUrl": "https://example.com",
  "event": "form.response.created",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rowform/latest/actions/subscribe-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hookUrl": "https://example.com",
    "event": "form.response.created",
    "formId": "string"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Subscribe Webhook action reference](actions/subscribe-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rowform/latest/actions/subscribe-webhook).
