# Seven Universal API Examples

These examples use the MindCloud API key and Seven connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance

Retrieves current account balance from Seven.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-balance?${params}`, {
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
      "amount": 1,
      "currency": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seven/latest/actions/get-balance).

## Create Contact

Creates a new contact in Seven.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seven/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seven/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "avatar": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "groups": [
        "string"
      ],
      "id": 1,
      "initials": {
        "color": "string",
        "initials": "string"
      },
      "properties": {
        "address": "string",
        "birthday": "string",
        "city": "string",
        "email": "ava@example.com",
        "firstname": "Ava",
        "home_number": "string",
        "lastname": "Chen",
        "mobile_number": "string",
        "notes": "string",
        "postal_code": "string"
      },
      "validation": {
        "state": "string",
        "timestamp": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seven/latest/actions/create-contact).
