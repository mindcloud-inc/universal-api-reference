# Escrow.com: Post Buyer Payment Details

Submits buyer payment details in Escrow.com.

```
POST https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/post-buyer-payment-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/post-buyer-payment-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/post-buyer-payment-details', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountName` | string | no | Name on the buyer bank account. |
| `bankName` | string | no | Name of the buyer's bank. |
| `bankState` | string | no | State or province for the buyer's bank. |
| `transactionId` | number | yes | The Escrow.com transaction ID. |
| `bankCountry` | string | no | Two-letter country code for the buyer's bank when paying by wire. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Escrow.com API returns.

## Native endpoint

Through the native Escrow.com API, this operation is `POST /transaction/:transaction_id/buyer_payment` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-buyer-payment-details.md) for the provider-specific parameters and requirements.

