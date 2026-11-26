# eBay: List Offers by SKU

Retrieves all existing offers for the specified SKU value. With options to limit the retrieved offers to a specific eBay marketplace, or a listing format.

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-offers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-offers?connectionId=$CONNECTION_ID&limit=25&offset=0&sku=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "sku": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-offers?${params}`, {
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
| `sku` | string | yes | The seller-defined SKU value. All offers associated with this product are returned in the response. |
| `format` | string | no | This value sets the listing format for the offers being retrieved. Pass this parameter when you only want to see offers in a specified listing format, such as FIXED_PRICE or AUCTION. |
| `marketplace_id` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableQuantity": 1,
      "categoryId": "string",
      "format": "string",
      "hideBuyerDetails": true,
      "includeCatalogProductDetails": true,
      "listingDuration": "string",
      "listingPolicies": {
        "eBayPlusIfEligible": true
      },
      "marketplaceId": "string",
      "merchantLocationKey": "string",
      "offerId": "string",
      "pricingSummary": {
        "price": {
          "currency": "string",
          "value": "string"
        }
      },
      "sku": "string",
      "status": "string",
      "tax": {
        "applyTax": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableQuantity` | number |  |
| `categoryId` | string |  |
| `format` | string |  |
| `hideBuyerDetails` | boolean |  |
| `includeCatalogProductDetails` | boolean |  |
| `listingDuration` | string |  |
| `listingPolicies.eBayPlusIfEligible` | boolean |  |
| `marketplaceId` | string |  |
| `merchantLocationKey` | string |  |
| `offerId` | string |  |
| `pricingSummary.price.currency` | string |  |
| `pricingSummary.price.value` | string |  |
| `sku` | string |  |
| `status` | string |  |
| `tax.applyTax` | boolean |  |

## Native endpoint

Through the native eBay API, this operation is `GET sell/inventory/v1/offer` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-offers.md) for the provider-specific parameters and requirements.

