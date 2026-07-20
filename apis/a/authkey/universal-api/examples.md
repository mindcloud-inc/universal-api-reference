# Authkey Universal API Examples

These examples use the MindCloud API key and Authkey connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance

Retrieves the current account balance from Authkey.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/authkey/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/authkey/latest/actions/get-balance?${params}`, {
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
      "balance": 1,
      "currency": "string",
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/authkey/latest/actions/get-balance).

## Send Email From Template

Sends a templated email through Authkey.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-email-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "apps@mindcloud.co",
  "mid": "1001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-email-from-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "apps@mindcloud.co",
    "mid": "1001"
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

See the full [Send Email From Template action reference](actions/send-email-from-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/authkey/latest/actions/send-email-from-template).
