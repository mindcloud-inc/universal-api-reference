# Mercado Pago: Search Subscription Plans

Finds subscription plans in Mercado Pago by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-subscription-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mercado Pago `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-subscription-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-subscription-plans?${params}`, {
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
| `status` | string | no | Default: `active`. |
| `q` | string | no |  |
| `sort` | string | no | Default: `date_created`. |
| `criteria` | string | no | Default: `asc`. |

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

Through the native Mercado Pago API, this operation is `GET /preapproval_plan/search` (base URL `https://api.mercadopago.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-subscription-plans.md) for the provider-specific parameters and requirements.

