# Prembly Universal API Examples

These examples use the MindCloud API key and Prembly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Wallet Balance

Retrieves a wallet balance from Prembly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-wallet-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-wallet-balance?${params}`, {
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
      "country_code": "string",
      "currency": "string",
      "email": "ava@example.com",
      "is_active": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Wallet Balance action reference](actions/get-wallet-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/prembly/latest/actions/get-wallet-balance).

## Account with Name Comparism

Creates account name comparism verification in Prembly.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/account-with-name-comparism" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/account-with-name-comparism', {
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
      "account_data": {
        "account_name": "Ava Chen",
        "account_number": "string",
        "bank_id": 1
      },
      "comparism_data": {
        "confidence": 1,
        "status": true
      },
      "detail": "string",
      "response_code": "string",
      "status": true,
      "verification": {
        "endpoint": "string",
        "reference": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Account with Name Comparism action reference](actions/account-with-name-comparism.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/prembly/latest/actions/account-with-name-comparism).
