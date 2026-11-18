# TikTok Shop: Get Product

Retrieve all properties of a product that is in the DRAFT, PENDING, or ACTIVATE status.

```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-product?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-product?${params}`, {
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
| `shopCipher` | list<string> | no | Use this property to pass shop information in requesting the API. Failure in passing the correct value when requesting the API for cross-border shops will return incorrect response. Get by API Get Authorization Shop |
| `return_under_review_version` | string | no | A flag to indicate what product information to retrieve if a live product (ACTIVATE status) is edited and resent for TikTok Shop review. - True: Retrieves the latest version of the product information that is currently under review. - False: Retrieves a snapshot of the product information that is live and online (before the edit). Default: False Default: `False`. |
| `product_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audit": {
        "notSubmittedReasons": [
          "string"
        ],
        "preApprovedReasons": [
          "string"
        ],
        "status": "string"
      },
      "categoryChains": [
        {
          "id": "string",
          "isLeaf": true,
          "localName": "Ava Chen",
          "parentId": "string"
        }
      ],
      "createTime": 1,
      "description": "string",
      "hasDraft": true,
      "id": "string",
      "isCodAllowed": true,
      "isNotForSale": true,
      "isPreOwned": true,
      "isReplicated": true,
      "listingQualityTier": "string",
      "mainImages": [
        {
          "height": 1,
          "thumbUrls": [
            "https://example.com"
          ],
          "uri": "string",
          "urls": [
            "https://example.com"
          ],
          "width": 1
        }
      ],
      "manufacturerIds": [
        "string"
      ],
      "packageDimensions": {
        "height": "string",
        "length": "string",
        "unit": "string",
        "width": "string"
      },
      "packageWeight": {
        "unit": "string",
        "value": "string"
      },
      "productAttributes": [
        {
          "id": "string",
          "name": "Ava Chen",
          "values": [
            {
              "id": "string",
              "name": "Ava Chen"
            }
          ]
        }
      ],
      "productStatus": "string",
      "productTags": [
        "string"
      ],
      "recommendedCategories": [
        "string"
      ],
      "responsiblePersonIds": [
        "string"
      ],
      "sellingFormat": "string",
      "shippingInsuranceRequirement": "string",
      "skus": [
        {
          "globalListingPolicy": {
            "inventoryType": "string",
            "priceSync": true
          },
          "id": "string",
          "inventory": [
            {
              "quantity": 1,
              "warehouseId": "string"
            }
          ],
          "price": {
            "currency": "string",
            "salePrice": "string",
            "taxExclusivePrice": "string"
          },
          "salesAttributes": [
            "string"
          ],
          "sellerSku": "string",
          "skuDimensions": {
            "height": "string",
            "length": "string",
            "unit": "string",
            "width": "string"
          },
          "skuWeight": {
            "unit": "string",
            "value": "string"
          },
          "statusInfo": {
            "status": "string"
          }
        }
      ],
      "status": "string",
      "subscribeInfo": {
        "subscribePromotionConfig": [
          {
            "discountLevel": "string",
            "discountOptions": [
              1
            ],
            "maxDiscount": 1,
            "minDiscount": 1
          }
        ],
        "subscribeStatus": "string",
        "supportSubscribe": true
      },
      "title": "string",
      "updateTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audit` | object |  |
| `audit.notSubmittedReasons` | array |  |
| `audit.preApprovedReasons` | array |  |
| `audit.status` | string |  |
| `categoryChains` | array<object> |  |
| `categoryChains[].id` | string |  |
| `categoryChains[].isLeaf` | boolean |  |
| `categoryChains[].localName` | string |  |
| `categoryChains[].parentId` | string |  |
| `createTime` | number |  |
| `description` | string |  |
| `hasDraft` | boolean |  |
| `id` | string |  |
| `isCodAllowed` | boolean |  |
| `isNotForSale` | boolean |  |
| `isPreOwned` | boolean |  |
| `isReplicated` | boolean |  |
| `listingQualityTier` | string |  |
| `mainImages` | array<object> |  |
| `mainImages[].height` | number |  |
| `mainImages[].thumbUrls` | array<string> |  |
| `mainImages[].uri` | string |  |
| `mainImages[].urls` | array<string> |  |
| `mainImages[].width` | number |  |
| `manufacturerIds` | array |  |
| `packageDimensions` | object |  |
| `packageDimensions.height` | string |  |
| `packageDimensions.length` | string |  |
| `packageDimensions.unit` | string |  |
| `packageDimensions.width` | string |  |
| `packageWeight` | object |  |
| `packageWeight.unit` | string |  |
| `packageWeight.value` | string |  |
| `productAttributes` | array<object> |  |
| `productAttributes[].id` | string |  |
| `productAttributes[].name` | string |  |
| `productAttributes[].values` | array<object> |  |
| `productAttributes[].values[].id` | string |  |
| `productAttributes[].values[].name` | string |  |
| `productStatus` | string |  |
| `productTags` | array |  |
| `recommendedCategories` | array |  |
| `responsiblePersonIds` | array |  |
| `sellingFormat` | string |  |
| `shippingInsuranceRequirement` | string |  |
| `skus` | array<object> |  |
| `skus[].globalListingPolicy` | object |  |
| `skus[].globalListingPolicy.inventoryType` | string |  |
| `skus[].globalListingPolicy.priceSync` | boolean |  |
| `skus[].id` | string |  |
| `skus[].inventory` | array<object> |  |
| `skus[].inventory[].quantity` | number |  |
| `skus[].inventory[].warehouseId` | string |  |
| `skus[].price` | object |  |
| `skus[].price.currency` | string |  |
| `skus[].price.salePrice` | string |  |
| `skus[].price.taxExclusivePrice` | string |  |
| `skus[].salesAttributes` | array |  |
| `skus[].sellerSku` | string |  |
| `skus[].skuDimensions` | object |  |
| `skus[].skuDimensions.height` | string |  |
| `skus[].skuDimensions.length` | string |  |
| `skus[].skuDimensions.unit` | string |  |
| `skus[].skuDimensions.width` | string |  |
| `skus[].skuWeight` | object |  |
| `skus[].skuWeight.unit` | string |  |
| `skus[].skuWeight.value` | string |  |
| `skus[].statusInfo` | object |  |
| `skus[].statusInfo.status` | string |  |
| `status` | string |  |
| `subscribeInfo` | object |  |
| `subscribeInfo.subscribePromotionConfig` | array<object> |  |
| `subscribeInfo.subscribePromotionConfig[].discountLevel` | string |  |
| `subscribeInfo.subscribePromotionConfig[].discountOptions` | array<number> |  |
| `subscribeInfo.subscribePromotionConfig[].maxDiscount` | number |  |
| `subscribeInfo.subscribePromotionConfig[].minDiscount` | number |  |
| `subscribeInfo.subscribeStatus` | string |  |
| `subscribeInfo.supportSubscribe` | boolean |  |
| `title` | string |  |
| `updateTime` | number |  |

## Native endpoint

Through the native TikTok Shop API, this operation is `GET product/202309/products/:product_id` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

