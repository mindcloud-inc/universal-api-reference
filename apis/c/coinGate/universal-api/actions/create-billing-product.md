# CoinGate: Create Billing Product

Creates a new billing product in CoinGate.

```
POST https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-billing-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-billing-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "price": "string",
  "currencyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-billing-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "price": "string",
    "currencyId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Billing product name. |
| `price` | string | yes | Billing product price. |
| `currencyId` | number | yes | CoinGate currency ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": {
        "id": 1
      },
      "id": 1,
      "name": "Ava Chen",
      "price": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `currency.id` | number |  |
| `id` | number |  |
| `name` | string |  |
| `price` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `POST /billing/products` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-billing-product.md) for the provider-specific parameters and requirements.

