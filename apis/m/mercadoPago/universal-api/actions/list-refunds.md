# Mercado Pago: List Refunds

Retrieves refunds for a payment from Mercado Pago.

```
GET https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/list-refunds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mercado Pago `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/list-refunds?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/list-refunds?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "refunds": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `refunds[]` | array<object> |  |
| `refunds[].id` | string |  |
| `refunds[].status` | string |  |

## Native endpoint

Through the native Mercado Pago API, this operation is `GET /v1/payments/{id}/refunds` (base URL `https://api.mercadopago.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-refunds.md) for the provider-specific parameters and requirements.

