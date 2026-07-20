# Mercado Pago: Update Merchant Order

Updates an existing merchant order in Mercado Pago.

```
PUT https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/update-merchant-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mercado Pago `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/update-merchant-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/update-merchant-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `external_reference` | string | no |  |
| `preference_id` | string | no |  |
| `marketplace` | string | no |  |
| `notification_url` | string | no | Use an HTTPS callback URL. |

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

Through the native Mercado Pago API, this operation is `PUT /merchant_orders/{id}` (base URL `https://api.mercadopago.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-merchant-order.md) for the provider-specific parameters and requirements.

