# Shopkit: List Coupons

Retrieves coupons from Shopkit.

```
GET https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-coupons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-coupons?${params}`, {
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
      "active": true,
      "applies_to": "string",
      "applies_to_clients": "string",
      "code": "string",
      "coupon": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "limit": 1,
      "orders_discount": 1,
      "orders_total": 1,
      "shareable_url": "https://example.com",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "used": 1,
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `applies_to` | string |  |
| `applies_to_clients` | string |  |
| `code` | string |  |
| `coupon` | string |  |
| `created_at` | date |  |
| `id` | number |  |
| `limit` | number |  |
| `orders_discount` | number |  |
| `orders_total` | number |  |
| `shareable_url` | string |  |
| `type` | string |  |
| `updated_at` | date |  |
| `used` | number |  |
| `value` | number |  |

## Native endpoint

Through the native Shopkit API, this operation is `GET /coupon` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-coupons.md) for the provider-specific parameters and requirements.

