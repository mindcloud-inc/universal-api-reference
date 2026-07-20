# Dukaan: List Discounts

Retrieves discounts from Dukaan.

```
GET https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-discounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-discounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-discounts?${params}`, {
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
| `search` | string | no | Discount/coupon search text. Example: `SUMMER20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "discount_type": 1,
      "discount_value": 1,
      "expiry_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_active": true,
      "is_hidden": true,
      "max_discount": 1,
      "min_order_value": 1,
      "modified_at": "2026-05-07T12:00:00.000Z",
      "start_date": "2026-05-07T12:00:00.000Z",
      "total_usage_count": 1,
      "uses_per_customer": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Discount code |
| `created_at` | date | Creation timestamp |
| `description` | string | Discount description |
| `discount_type` | number | Discount type code |
| `discount_value` | number | Discount amount or percentage |
| `expiry_date` | date | Discount expiry timestamp |
| `id` | number | Dukaan discount ID |
| `is_active` | boolean | Whether the discount is active |
| `is_hidden` | boolean | Whether the discount is hidden |
| `max_discount` | number | Maximum discount amount |
| `min_order_value` | number | Minimum order value |
| `modified_at` | date | Last modified timestamp |
| `start_date` | date | Discount start timestamp |
| `total_usage_count` | number | Total usage count |
| `uses_per_customer` | number | Allowed uses per customer |
| `uuid` | string | Dukaan discount UUID |

## Native endpoint

Through the native Dukaan API, this operation is `GET api/coupon/seller/coupon/v2/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-discounts.md) for the provider-specific parameters and requirements.

