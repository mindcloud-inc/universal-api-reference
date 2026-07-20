# Becon: Create BTC Test Payment

Creates a Bitcoin test payment in Becon.

```
POST https://connect.mindcloud.co/v1/universal/becon/latest/actions/create-btc-test-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/becon/latest/actions/create-btc-test-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "1bc34t3grrr33",
  "currency_id": "1",
  "store_id": "216",
  "sum": "string",
  "transaction_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/becon/latest/actions/create-btc-test-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "1bc34t3grrr33",
    "currency_id": "1",
    "store_id": "216",
    "sum": "string",
    "transaction_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | yes | The destination crypto address for the sandbox payment. Default: `1bc34t3grrr33`. |
| `currency_id` | string | yes | The Becon currency ID for the test payment. Default: `1`. |
| `store_id` | string | yes | The Becon store ID that owns the test payment. Default: `216`. |
| `sum` | string | yes | The crypto amount to send in the sandbox payment. |
| `transaction_id` | string | yes | The external transaction ID used by the test payment request. |

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
| `message` | string | Provider status message. |

## Native endpoint

Through the native Becon API, this operation is `POST /v1/test` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-btc-test-payment.md) for the provider-specific parameters and requirements.

