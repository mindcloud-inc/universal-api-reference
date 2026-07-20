# e-Boekhouden.nl: Create Product

Creates a new product in e-Boekhouden.nl.

```
POST https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Boekhouden.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string",
  "description": "string",
  "vat": "string",
  "ledgerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string",
    "description": "string",
    "vat": "string",
    "ledgerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | The code of the product. Error codes ART_004 Product Code is missing. ART_007 Product Code is too long. |
| `description` | string | yes | The description of the product. Error codes ART_005 Product Description is missing. |
| `unitId` | number | no | The unit ID of the product. Error codes ART_011 Product Unit could not be found. |
| `active` | boolean | no | Whether the product is active. |
| `groupId` | number | no | The group ID of the product. Error codes ART_012 Product Group could not be found. |
| `purchasePriceExcl` | number | no | The purchase price (excluding VAT) of the product. Error codes ART_027 The value of PurchasePriceExcl exceeds the maximum value of 999999999999.00. ART_032 The value of PurchasePriceExcl is below the minimum value of -999999999999.00. |
| `priceExcl` | number | no | The price (excluding VAT) of the product. This field can not be combined with `priceIncl`. Error codes ART_018 Either priceExcl or priceIncl is required. ART_019 Both priceExcl and priceIncl are required with current VAT code. ART_024 The value of PriceExcl exceeds the maximum value of 999999999999.00. ART_026 The value of PriceIncl after applying VAT exceeds the maximum value of 999999999999.00. ART_029 The value of PriceExcl is below the minimum value of -999999999999.00. ART_031 The value of PriceIncl after applying VAT is below the minimum value of -999999999999.00. |
| `priceIncl` | number | no | The price (including VAT) of the product. This field can not be combined with `priceExcl`. Error codes ART_016 priceIncl cannot have a value when priceExcl is passed. ART_018 Either priceExcl or priceIncl is required. ART_019 Both priceExcl and priceIncl are required with current VAT code. ART_025 The value of PriceIncl exceeds the maximum value of 999999999999.00. ART_030 The value of PriceIncl is below the minimum value of -999999999999.00. |
| `vat` | string | yes | The VAT code of the product. Only supports VAT codes of type 'Sale'. Error codes ART_013 Product VAT code could not be found. ART_017 Product VAT code is required. |
| `ledgerId` | number | yes | The ledger ID of the product. Error codes ART_006 Product Ledger ID is missing. ART_009 Product Ledger could not be found. ART_028 Ledger category must be 'BAL' or 'VW'. |
| `costCenterId` | number | no | The cost center ID of the product. Error codes ART_010 Product Cost center is inactive. ART_015 Product cost center could not be found. |
| `inStockManagement` | boolean | no | Whether the product will be Included in automatic inventory management. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native e-Boekhouden.nl API returns.

## Native endpoint

Through the native e-Boekhouden.nl API, this operation is `POST /v1/product` (base URL `https://api.e-boekhouden.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

