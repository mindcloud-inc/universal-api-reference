# Dukaan: Create Discount

Creates a new discount in Dukaan.

```
POST https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-discount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-discount" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "SUMMER20",
  "discountValue": "20"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-discount', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "SUMMER20",
    "discountValue": "20"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | Discount code. Example: `SUMMER20`. |
| `discountValue` | string | yes | Discount value. Example: `20`. |
| `minOrderValue` | string | no | Minimum order value. Example: `500`. |
| `discountType` | number | no | Dukaan discount type code. Default: `0`. |
| `autoApply` | boolean | no | Whether Dukaan should auto-apply the coupon. Default: `true`. |
| `isActive` | boolean | no | Whether the discount is active. Default: `true`. |
| `startDate` | date | no | Discount start date/time. |
| `expiryDate` | date | no | Discount expiry date/time. |
| `maxDiscount` | string | no | Maximum discount amount. Example: `100`. |

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

Through the native Dukaan API, this operation is `POST api/coupon/seller/coupon/v2/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-discount.md) for the provider-specific parameters and requirements.

