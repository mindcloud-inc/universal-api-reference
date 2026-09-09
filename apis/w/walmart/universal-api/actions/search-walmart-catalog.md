# Walmart: Search Walmart Catalog

Search the Walmart.com global product catalog by item keyword, UPC or GTIN.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/search-walmart-catalog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/search-walmart-catalog?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/search-walmart-catalog?${params}`, {
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
| `query` | string | no | This parameter allows you to perform a general search based on descriptive terms related to the product. Example: `keyboard and mouse` |
| `upc` | string | no | Search by the 12-digit Universal Product Code (UPC). |
| `gtin` | string | no | Search by the 14-digit Global Trade Item Number (GTIN). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": "string",
      "condition": "string",
      "customerRating": "string",
      "description": "string",
      "images": [
        {
          "url": "https://example.com"
        }
      ],
      "isMarketPlaceItem": true,
      "itemId": "string",
      "price": {
        "amount": "string",
        "currency": "string"
      },
      "productType": "string",
      "properties": {
        "categories": [
          "string"
        ],
        "nextDayEligible": true,
        "numReviews": "string",
        "variantItemsNum": "string",
        "variants": {
          "variantData": [
            {
              "isAvailable": "string",
              "itemId": "string",
              "productImageUrl": "https://example.com",
              "title": "string",
              "variantValues": [
                {
                  "name": "Ava Chen",
                  "value": "string"
                }
              ]
            }
          ],
          "variantMeta": [
            {
              "name": "Ava Chen"
            }
          ]
        }
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | string |  |
| `condition` | string |  |
| `customerRating` | string |  |
| `description` | string |  |
| `images[].url` | string |  |
| `isMarketPlaceItem` | boolean |  |
| `itemId` | string |  |
| `price.amount` | string |  |
| `price.currency` | string |  |
| `productType` | string |  |
| `properties.categories[]` | string |  |
| `properties.nextDayEligible` | boolean |  |
| `properties.numReviews` | string |  |
| `properties.variantItemsNum` | string |  |
| `properties.variants.variantData[].isAvailable` | string |  |
| `properties.variants.variantData[].itemId` | string |  |
| `properties.variants.variantData[].productImageUrl` | string |  |
| `properties.variants.variantData[].title` | string |  |
| `properties.variants.variantData[].variantValues[].name` | string |  |
| `properties.variants.variantData[].variantValues[].value` | string |  |
| `properties.variants.variantMeta[].name` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/items/walmart/search` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-walmart-catalog.md) for the provider-specific parameters and requirements.

