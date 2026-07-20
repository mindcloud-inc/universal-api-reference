# Boomlify Universal API Examples

These examples use the MindCloud API key and Boomlify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves account information from Boomlify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-info?${params}`, {
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
      "account": {
        "api_key_prefix": "string",
        "credits_balance": 1,
        "email": "ava@example.com",
        "member_since": "2026-05-07T12:00:00.000Z",
        "tier": "string",
        "user_id": "string"
      },
      "features": {},
      "meta": {
        "request_time": "2026-05-07T12:00:00.000Z"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boomlify/latest/actions/get-account-info).

## Bulk Enable Dashboard Telegram Forwarding

Bulk enables Telegram forwarding for owned mailboxes in Boomlify.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/bulk-enable-dashboard-telegram-forwarding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailIds[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/bulk-enable-dashboard-telegram-forwarding', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailIds[]": ["ava@example.com"]
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
      "emailId": "ava@example.com",
      "id": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Bulk Enable Dashboard Telegram Forwarding action reference](actions/bulk-enable-dashboard-telegram-forwarding.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boomlify/latest/actions/bulk-enable-dashboard-telegram-forwarding).
