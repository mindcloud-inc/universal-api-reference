# Poof: Send Transaction

Creates a new payout transaction in Poof.

```
POST https://connect.mindcloud.co/v1/universal/poof/latest/actions/send-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/poof/latest/actions/send-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": "0.2",
  "crypto": "solana",
  "address": "EREWUKBjJhxmFRFeh3gHjQTbbBxZGL1yiioiVG7wA6K6"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/poof/latest/actions/send-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": "0.2",
    "crypto": "solana",
    "address": "EREWUKBjJhxmFRFeh3gHjQTbbBxZGL1yiioiVG7wA6K6"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Payout amount. Default: `0.2`. |
| `crypto` | string | yes | Crypto asset code. Default: `solana`. |
| `address` | string | yes | Destination wallet address. Default: `EREWUKBjJhxmFRFeh3gHjQTbbBxZGL1yiioiVG7wA6K6`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Poof API, this operation is `POST /payouts` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transaction.md) for the provider-specific parameters and requirements.

