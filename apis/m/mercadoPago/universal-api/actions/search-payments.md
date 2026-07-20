# Mercado Pago: Search Payments

Finds payments in Mercado Pago by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mercado Pago `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-payments?connectionId=$CONNECTION_ID&sort=date_created&criteria=desc&external_reference=string&range=date_created" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sort": "date_created",
  "criteria": "desc",
  "external_reference": "string",
  "range": "date_created"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-payments?${params}`, {
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
| `sort` | string | yes | Default: `date_created`. |
| `criteria` | string | yes | Default: `desc`. |
| `external_reference` | string | yes |  |
| `range` | string | yes | Default: `date_created`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `begin_date` | string | no |  |
| `end_date` | string | no |  |
| `store_id` | number | no |  |
| `pos_id` | number | no |  |
| `collector.id` | number | no |  |
| `payer.id` | number | no |  |
| `installments` | number | no |  |
| `payment_method_id` | string | no |  |
| `payment_type_id` | string | no |  |
| `operation_type` | string | no |  |
| `processing_mode` | string | no |  |
| `status` | string | no |  |
| `status_detail` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paging": {
        "limit": 1,
        "offset": 1,
        "total": 1
      },
      "results": [
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
| `paging.limit` | number |  |
| `paging.offset` | number |  |
| `paging.total` | number |  |
| `results[]` | array<object> |  |

## Native endpoint

Through the native Mercado Pago API, this operation is `GET /v1/payments/search` (base URL `https://api.mercadopago.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-payments.md) for the provider-specific parameters and requirements.

