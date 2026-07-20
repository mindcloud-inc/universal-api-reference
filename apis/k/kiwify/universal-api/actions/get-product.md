# Kiwify: Get Product

Retrieves a product from Kiwify.

```
GET https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/get-product?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/get-product?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate_enabled": true,
      "bumps": [
        {}
      ],
      "created_at": "string",
      "currency": "string",
      "event_batches": [
        {}
      ],
      "event_settings": {},
      "id": "string",
      "links": [
        {}
      ],
      "name": "Ava Chen",
      "offers": [
        {}
      ],
      "payment_type": "string",
      "price": 1,
      "revenue_partners": [
        {}
      ],
      "status": "string",
      "subscriptions": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate_enabled` | boolean |  |
| `bumps` | array<object> |  |
| `created_at` | string |  |
| `currency` | string |  |
| `event_batches` | array<object> |  |
| `event_settings` | object |  |
| `id` | string |  |
| `links` | array<object> |  |
| `name` | string |  |
| `offers` | array<object> |  |
| `payment_type` | string |  |
| `price` | number |  |
| `revenue_partners` | array<object> |  |
| `status` | string |  |
| `subscriptions` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Kiwify API, this operation is `GET /v1/products/:id` (base URL `https://public-api.kiwify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

