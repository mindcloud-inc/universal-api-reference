# Mercado Pago: List Payment Methods

Retrieves payment methods from Mercado Pago.

```
GET https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/list-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mercado Pago `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/list-payment-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/list-payment-methods?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "payment_type_id": "string",
      "secure_thumbnail": "string",
      "status": "string",
      "thumbnail": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `payment_type_id` | string |  |
| `secure_thumbnail` | string |  |
| `status` | string |  |
| `thumbnail` | string |  |

## Native endpoint

Through the native Mercado Pago API, this operation is `GET /v1/payment_methods` (base URL `https://api.mercadopago.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-methods.md) for the provider-specific parameters and requirements.

