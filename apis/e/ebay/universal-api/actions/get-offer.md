# eBay: Get Offer

Retrieve an Offer by it's unique offer ID.

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-offer?connectionId=$CONNECTION_ID&offerID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "offerID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-offer?${params}`, {
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
| `offerID` | string | yes | The unique ID of an offer to retrieve. Use the "List Offers by SKU" action to retrieve offer IDs. |

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

Through the native eBay API, this operation is `GET sell/inventory/v1/offer/:offerID` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-offer.md) for the provider-specific parameters and requirements.

