# Strale Universal API Examples

These examples use the MindCloud API key and Strale connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Wallet Balance

Retrieves your wallet balance from Strale.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-wallet-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-wallet-balance?${params}`, {
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
      "balanceCents": 1,
      "currency": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Wallet Balance action reference](actions/get-wallet-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/strale/latest/actions/get-wallet-balance).

## Create Wallet Top-Up

Creates a wallet top-up checkout session in Strale.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/strale/latest/actions/create-wallet-top-up" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount_cents": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/strale/latest/actions/create-wallet-top-up', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount_cents": 1
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
      "amountCents": 1,
      "checkoutUrl": "https://example.com",
      "sessionId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Wallet Top-Up action reference](actions/create-wallet-top-up.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/strale/latest/actions/create-wallet-top-up).
