# WooCommerce Universal API Examples

These examples use the MindCloud API key and WooCommerce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves products from WooCommerce.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/list-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "averageRating": "string",
      "catalogVisibility": "string",
      "categories": [
        {}
      ],
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateCreatedGmt": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "dateModifiedGmt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dimensions": {},
      "downloadable": true,
      "featured": true,
      "hasOptions": true,
      "id": 1,
      "images": [
        {}
      ],
      "menuOrder": 1,
      "name": "Ava Chen",
      "onSale": true,
      "parentId": 1,
      "permalink": "https://example.com",
      "price": "string",
      "purchasable": true,
      "ratingCount": 1,
      "regularPrice": "string",
      "reviewsAllowed": true,
      "salePrice": "string",
      "shippingRequired": true,
      "shippingTaxable": true,
      "shortDescription": "string",
      "sku": "string",
      "slug": "string",
      "status": "string",
      "stockStatus": "string",
      "tags": [
        {}
      ],
      "totalSales": 1,
      "type": "string",
      "virtual": true
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wooCommerce/latest/actions/list-products).

## Create Coupon

Creates a new coupon in WooCommerce.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-coupon', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Create Coupon action reference](actions/create-coupon.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wooCommerce/latest/actions/create-coupon).
