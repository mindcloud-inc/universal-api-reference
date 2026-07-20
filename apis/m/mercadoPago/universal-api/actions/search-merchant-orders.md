# Mercado Pago: Search Merchant Orders

Finds merchant orders in Mercado Pago by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-merchant-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mercado Pago `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-merchant-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-merchant-orders?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no |  |
| `preference_id` | string | no |  |
| `application_id` | number | no |  |
| `payer_id` | number | no |  |
| `sponsor_id` | number | no |  |
| `external_reference` | string | no |  |
| `site_id` | string | no |  |
| `marketplace` | string | no |  |
| `date_created_from` | string | no |  |
| `date_created_to` | string | no |  |
| `last_updated_from` | string | no |  |
| `last_updated_to` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elements": [
        [
          {}
        ]
      ],
      "next_offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elements[]` | array<object> |  |
| `next_offset` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Mercado Pago API, this operation is `GET /merchant_orders/search` (base URL `https://api.mercadopago.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-merchant-orders.md) for the provider-specific parameters and requirements.

