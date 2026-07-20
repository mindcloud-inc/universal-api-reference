# Mercado Pago: Search Claims

Finds claims in Mercado Pago by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-claims
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mercado Pago `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-claims?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-claims?${params}`, {
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
| `id` | number | no |  |
| `type` | string | no |  |
| `stage` | string | no |  |
| `status` | string | no |  |
| `resource` | string | no |  |
| `resource_id` | number | no |  |

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

Through the native Mercado Pago API, this operation is `GET /post-purchase/v1/claims/search` (base URL `https://api.mercadopago.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-claims.md) for the provider-specific parameters and requirements.

