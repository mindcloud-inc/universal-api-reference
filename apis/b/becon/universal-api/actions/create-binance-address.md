# Becon: Create Binance Address

Creates a new Binance payment address in Becon.

```
POST https://connect.mindcloud.co/v1/universal/becon/latest/actions/create-binance-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/becon/latest/actions/create-binance-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chain": "binance",
  "external_id": "string",
  "origin_amount": "string",
  "origin_currency": "string",
  "payment_currency": "BNB"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/becon/latest/actions/create-binance-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chain": "binance",
    "external_id": "string",
    "origin_amount": "string",
    "origin_currency": "string",
    "payment_currency": "BNB"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chain` | string | yes | Fixed target network for this preset. Default: `binance`. |
| `external_id` | string | yes | Unique tracking value returned in callbacks. |
| `origin_amount` | string | yes | Amount in the origin currency for automatic conversion. |
| `origin_currency` | string | yes | Origin fiat currency, for example USD or EUR. |
| `payment_currency` | string | yes | Token ticker to accept, for example BNB. Default: `BNB`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "message": "string",
      "payment_amount": "string",
      "payment_currency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | New payment address. |
| `message` | string | Provider message. |
| `payment_amount` | string | Amount that must be paid. |
| `payment_currency` | string | Token ticker to pay. |

## Native endpoint

Through the native Becon API, this operation is `POST /v2/address` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-binance-address.md) for the provider-specific parameters and requirements.

