# e-Boekhouden.nl: Update Product

Updates a product in e-Boekhouden.nl.

```
PUT https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Boekhouden.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-product', {
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
| `id` | number | yes |  |
| `code` | string | no | The code of the product. Error codes ART_004 Product Code is missing. ART_007 Product Code is too long. |
| `description` | string | no | The description of the product. Error codes ART_005 Product Description is missing. |
| `unitId` | number | no | The unit ID of the product. Error codes ART_011 Product Unit could not be found. |
| `active` | boolean | no | Whether the product is active. |
| `groupId` | number | no | The group ID of the product. Error codes ART_012 Product Group could not be found. |
| `purchasePriceExcl` | number | no | The purchase price (excluding VAT) of the product. Error codes ART_027 The value of PurchasePriceExcl exceeds the maximum value of 999999999999.00. ART_032 The value of PurchasePriceExcl is below the minimum value of -999999999999.00. |
| `priceExcl` | number | no | The price (excluding VAT) of the product. This field can not be combined with `priceIncl`. Error codes ART_021 priceExcl cannot be null or empty. ART_024 The value of PriceExcl exceeds the maximum value of 999999999999.00. ART_026 The value of PriceIncl after applying VAT exceeds the maximum value of 999999999999.00. ART_029 The value of PriceExcl is below the minimum value of -999999999999.00. ART_031 The value of PriceIncl after applying VAT is below the minimum value of -999999999999.00. |
| `priceIncl` | number | no | The price (including VAT) of the product. This field can not be combined with `priceExcl`. Error codes ART_016 priceIncl cannot have a value when priceExcl is passed. ART_020 priceIncl cannot be null or empty. ART_025 The value of PriceIncl exceeds the maximum value of 999999999999.00. ART_030 The value of PriceIncl is below the minimum value of -999999999999.00. |
| `vat` | string | no | The VAT code of the product. Only supports VAT codes of type 'Sale'. Error codes ART_013 Product VAT code could not be found. ART_022 VAT code cannot be null or empty. |
| `ledgerId` | number | no | The ledger ID of the product. Error codes ART_006 Product Ledger ID is missing. ART_009 Product Ledger could not be found. ART_028 Ledger category must be 'BAL' or 'VW'. |
| `costCenterId` | number | no | The cost center ID of the product. Error codes ART_010 Product Cost center is inactive. ART_015 Product cost center could not be found. |
| `inStockManagement` | boolean | no | Whether the product will be Included in automatic inventory management. |
| `updateSubscriptions` | string | no | Specifies the level of changes to be applied to existing subscriptions when a product is updated. \| Value \| Description \| \|---\|---\| \| 0 \| No changes will be applied. \| \| 1 \| Only price changes will be applied. \| \| 2 \| All changes will be applied. \| |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native e-Boekhouden.nl API returns.

## Native endpoint

Through the native e-Boekhouden.nl API, this operation is `PATCH /v1/product/:id` (base URL `https://api.e-boekhouden.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

