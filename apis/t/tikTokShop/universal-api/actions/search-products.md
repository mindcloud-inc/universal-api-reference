# TikTok Shop: Search Products



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-products?connectionId=$CONNECTION_ID&limit=25&offset=0&shopCipher=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "shopCipher": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-products?${params}`, {
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
| `skuIds[]` | array<string> | no |  |
| `sellerSkus[]` | array<string> | no |  |
| `status` | string | no | Filter products by their status. Default: ALL Possible values: - ALL - DRAFT - PENDING - FAILED - ACTIVATE - SELLER_DEACTIVATED - PLATFORM_DEACTIVATED - FREEZE - DELETED |
| `shopCipher` | list<string> | yes |  |
| `sortField` | string | no |  |
| `sortOrder` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audit_status": [
        "string"
      ],
      "category_version": "string",
      "create_time_ge": 1,
      "create_time_le": 1,
      "listing_platforms": [
        "string"
      ],
      "listing_quality_tiers": [
        "string"
      ],
      "return_draft_version": true,
      "seller_skus": [
        "string"
      ],
      "sku_ids": [
        "string"
      ],
      "sns_filter": "string",
      "status": "string",
      "update_time_ge": 1,
      "update_time_le": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audit_status` | array |  |
| `category_version` | string |  |
| `create_time_ge` | number |  |
| `create_time_le` | number |  |
| `listing_platforms` | array |  |
| `listing_quality_tiers` | array |  |
| `return_draft_version` | boolean |  |
| `seller_skus` | array |  |
| `sku_ids` | array |  |
| `sns_filter` | string |  |
| `status` | string |  |
| `update_time_ge` | number |  |
| `update_time_le` | number |  |

## Native endpoint

Through the native TikTok Shop API, this operation is `POST product/202502/products/search` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-products.md) for the provider-specific parameters and requirements.

