# Mercado Pago: Create Cancellation

Cancels a payment in Mercado Pago.

```
PUT https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/create-cancellation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mercado Pago `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/create-cancellation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payment_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/create-cancellation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payment_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payment_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Mercado Pago API, this operation is `PUT /v1/payments/{payment_id}` (base URL `https://api.mercadopago.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-cancellation.md) for the provider-specific parameters and requirements.

