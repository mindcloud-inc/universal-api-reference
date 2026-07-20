# WooCommerce: Retrieve Coupon

Retrieves a coupon from WooCommerce.

```
GET https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/retrieve-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/retrieve-coupon?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/retrieve-coupon?${params}`, {
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
| `id` | list<number> | yes | Unique numeric ID of the coupon to retrieve. |

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

Through the native WooCommerce API, this operation is `GET /coupons/:id` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-coupon.md) for the provider-specific parameters and requirements.

