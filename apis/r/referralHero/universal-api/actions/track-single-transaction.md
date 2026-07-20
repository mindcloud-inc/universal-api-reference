# ReferralHero: Track Single Transaction

Creates a transaction for a subscriber in ReferralHero.

```
POST https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/track-single-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReferralHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/track-single-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "email": "ava@example.com",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/track-single-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "email": "ava@example.com",
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Transaction amount. |
| `email` | string | yes | Subscriber email. |
| `transactionId` | string | no | Unique transaction ID. |
| `uuid` | string | yes | ReferralHero list UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "id": 1,
      "productId": "string",
      "response": "string",
      "transactionId": "string",
      "transactionTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `id` | number |  |
| `productId` | string |  |
| `response` | string |  |
| `transactionId` | string |  |
| `transactionTime` | string |  |

## Native endpoint

Through the native ReferralHero API, this operation is `POST /lists/:uuid/subscribers/add_transactions` (base URL `https://app.referralhero.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-single-transaction.md) for the provider-specific parameters and requirements.

