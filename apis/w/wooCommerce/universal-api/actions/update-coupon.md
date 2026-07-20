# WooCommerce: Update Coupon

Updates an existing coupon in WooCommerce.

```
PUT https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/update-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/update-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/update-coupon', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | list<number> | yes | Unique numeric ID of the coupon to update. |
| `code` | string | no | Coupon code string. |
| `amount` | string | no | Discount amount as a string. |
| `discountType` | list<string> | no | Coupon discount type such as percent, fixed_cart, or fixed_product. One of: `fixed_cart`, `fixed_product`, `percent`. |
| `description` | string | no | Coupon description. |
| `dateExpires` | date | no | Expiration date for the coupon. |
| `individualUse` | boolean | no |  |
| `excludeSaleItems` | boolean | no |  |
| `minimumAmount` | string | no |  |
| `maximumAmount` | string | no |  |
| `freeShipping` | boolean | no |  |
| `usageLimit` | number | no |  |
| `usageLimitPerUser` | number | no |  |
| `productIds[]` | array<number> | no |  |
| `excludedProductIds[]` | array<number> | no |  |
| `emailRestrictions[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "code": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateCreatedGmt": "2026-05-07T12:00:00.000Z",
      "dateExpires": "2026-05-07T12:00:00.000Z",
      "dateExpiresGmt": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "dateModifiedGmt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "discountType": "string",
      "emailRestrictions": [
        "ava@example.com"
      ],
      "excludedProductCategories": [
        1
      ],
      "excludedProductIds": [
        1
      ],
      "excludeSaleItems": true,
      "freeShipping": true,
      "id": 1,
      "individualUse": true,
      "maximumAmount": "string",
      "metaData": [
        {}
      ],
      "minimumAmount": "string",
      "productCategories": [
        1
      ],
      "productIds": [
        1
      ],
      "status": "string",
      "usageCount": 1,
      "usedBy": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `code` | string |  |
| `dateCreated` | date |  |
| `dateCreatedGmt` | date |  |
| `dateExpires` | date |  |
| `dateExpiresGmt` | date |  |
| `dateModified` | date |  |
| `dateModifiedGmt` | date |  |
| `description` | string |  |
| `discountType` | string |  |
| `emailRestrictions` | array<string> |  |
| `excludedProductCategories` | array<number> |  |
| `excludedProductIds` | array<number> |  |
| `excludeSaleItems` | boolean |  |
| `freeShipping` | boolean |  |
| `id` | number |  |
| `individualUse` | boolean |  |
| `maximumAmount` | string |  |
| `metaData` | array<object> |  |
| `minimumAmount` | string |  |
| `productCategories` | array<number> |  |
| `productIds` | array<number> |  |
| `status` | string |  |
| `usageCount` | number |  |
| `usedBy` | array<string> |  |

## Native endpoint

Through the native WooCommerce API, this operation is `PUT /coupons/:id` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-coupon.md) for the provider-specific parameters and requirements.

