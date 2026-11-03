# Rithum for Brands: List Order Items



```
GET https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-order-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-order-items?connectionId=$CONNECTION_ID&limit=25&offset=0&orderID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "orderID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-order-items?${params}`, {
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
| `orderID` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "giftMessage": {},
      "giftNotes": {},
      "giftPrice": 1,
      "giftTaxPrice": 1,
      "harmonizedCode": {},
      "id": 1,
      "isBundle": true,
      "itemURL": "https://example.com",
      "orderID": 1,
      "productID": 1,
      "profileID": 1,
      "quantity": 1,
      "recyclingFee": 1,
      "referenceProductID": {},
      "referenceSku": {},
      "sellerOrderItemID": {},
      "shippingPrice": 1,
      "shippingTaxPrice": 1,
      "siteListingID": "string",
      "siteOrderItemID": "string",
      "sku": "string",
      "taxPrice": 1,
      "title": "string",
      "unitEstimatedShippingCost": 1,
      "unitPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `giftMessage` | object |  |
| `giftNotes` | object |  |
| `giftPrice` | number |  |
| `giftTaxPrice` | number |  |
| `harmonizedCode` | object |  |
| `id` | number |  |
| `isBundle` | boolean |  |
| `itemURL` | string |  |
| `orderID` | number |  |
| `productID` | number |  |
| `profileID` | number |  |
| `quantity` | number |  |
| `recyclingFee` | number |  |
| `referenceProductID` | object |  |
| `referenceSku` | object |  |
| `sellerOrderItemID` | object |  |
| `shippingPrice` | number |  |
| `shippingTaxPrice` | number |  |
| `siteListingID` | string |  |
| `siteOrderItemID` | string |  |
| `sku` | string |  |
| `taxPrice` | number |  |
| `title` | string |  |
| `unitEstimatedShippingCost` | number |  |
| `unitPrice` | number |  |

## Native endpoint

Through the native Rithum for Brands API, this operation is `GET Orders(:orderID)/Items` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-order-items.md) for the provider-specific parameters and requirements.

