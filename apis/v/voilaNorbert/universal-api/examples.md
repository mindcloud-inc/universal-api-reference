# VoilaNorbert Universal API Examples

These examples use the MindCloud API key and VoilaNorbert connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves current account details from VoilaNorbert.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-account?${params}`, {
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
      "admin": true,
      "api_token": "string",
      "avatar_url": "https://example.com",
      "created": "2026-05-07T12:00:00.000Z",
      "credits": {
        "charge_failed": 1,
        "refill_credits": 1,
        "refill_limit": 1,
        "refill_price": 1,
        "remains": 1,
        "total": 1
      },
      "email": "ava@example.com",
      "firstname": "Ava",
      "has_cc": true,
      "is_account_verified": true,
      "language": "string",
      "name": "Ava Chen",
      "optin": true
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voilaNorbert/latest/actions/get-account).

## Create List

Creates a new list in VoilaNorbert.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "contacts": 1,
      "created": 1,
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create List action reference](actions/create-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voilaNorbert/latest/actions/create-list).
