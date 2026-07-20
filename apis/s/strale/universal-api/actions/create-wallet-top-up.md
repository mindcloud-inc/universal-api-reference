# Strale: Create Wallet Top-Up

Creates a wallet top-up checkout session in Strale.

```
POST https://connect.mindcloud.co/v1/universal/strale/latest/actions/create-wallet-top-up
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount_cents` | number | yes | Top-up amount in euro cents. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountCents` | number | Requested top-up amount in cents. |
| `checkoutUrl` | string | Stripe Checkout URL for the wallet top-up session. |
| `sessionId` | string | Created checkout session identifier. |

## Native endpoint

Through the native Strale API, this operation is `POST /v1/wallet/topup` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-wallet-top-up.md) for the provider-specific parameters and requirements.

