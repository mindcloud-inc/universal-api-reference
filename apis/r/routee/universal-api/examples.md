# Routee Universal API Examples

These examples use the MindCloud API key and Routee connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Account Balance

Retrieves your current Routee account balance.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-account-balance?${params}`, {
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
      "currency": {
        "code": "string",
        "name": "Ava Chen",
        "sign": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Check Account Balance action reference](actions/check-account-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/routee/latest/actions/check-account-balance).

## Activate a sender

Activates an existing sender in Routee.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/activate-a-sender" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/activate-a-sender', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "code": "string"
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

See the full [Activate a sender action reference](actions/activate-a-sender.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/routee/latest/actions/activate-a-sender).
