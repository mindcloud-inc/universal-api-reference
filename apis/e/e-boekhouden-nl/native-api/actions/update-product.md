# Update Product with e-Boekhouden.nl

Updates a product in e-Boekhouden.nl.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/product/:id`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [Update Product](https://api.e-boekhouden.nl/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `code` | body | `string` | no | The code of the product. Error codes ART_004 Product Code is missing. ART_007 Product Code is too long. |
| `description` | body | `string` | no | The description of the product. Error codes ART_005 Product Description is missing. |
| `unitId` | body | `number` | no | The unit ID of the product. Error codes ART_011 Product Unit could not be found. |
| `active` | body | `boolean` | no | Whether the product is active. |
| `groupId` | body | `number` | no | The group ID of the product. Error codes ART_012 Product Group could not be found. |
| `purchasePriceExcl` | body | `number` | no | The purchase price (excluding VAT) of the product. Error codes ART_027 The value of PurchasePriceExcl exceeds the maximum value of 999999999999.00. ART_032 The value of PurchasePriceExcl is below the minimum value of -999999999999.00. |
| `priceExcl` | body | `number` | no | The price (excluding VAT) of the product. This field can not be combined with `priceIncl`. Error codes ART_021 priceExcl cannot be null or empty. ART_024 The value of PriceExcl exceeds the maximum value of 999999999999.00. ART_026 The value of PriceIncl after applying VAT exceeds the maximum value of 999999999999.00. ART_029 The value of PriceExcl is below the minimum value of -999999999999.00. ART_031 The value of PriceIncl after applying VAT is below the minimum value of -999999999999.00. |
| `priceIncl` | body | `number` | no | The price (including VAT) of the product. This field can not be combined with `priceExcl`. Error codes ART_016 priceIncl cannot have a value when priceExcl is passed. ART_020 priceIncl cannot be null or empty. ART_025 The value of PriceIncl exceeds the maximum value of 999999999999.00. ART_030 The value of PriceIncl is below the minimum value of -999999999999.00. |
| `vat` | body | `string` | no | The VAT code of the product. Only supports VAT codes of type 'Sale'. Error codes ART_013 Product VAT code could not be found. ART_022 VAT code cannot be null or empty. |
| `ledgerId` | body | `number` | no | The ledger ID of the product. Error codes ART_006 Product Ledger ID is missing. ART_009 Product Ledger could not be found. ART_028 Ledger category must be 'BAL' or 'VW'. |
| `costCenterId` | body | `number` | no | The cost center ID of the product. Error codes ART_010 Product Cost center is inactive. ART_015 Product cost center could not be found. |
| `inStockManagement` | body | `boolean` | no | Whether the product will be Included in automatic inventory management. |
| `updateSubscriptions` | body | `string` | no | Specifies the level of changes to be applied to existing subscriptions when a product is updated. \| Value \| Description \| \|---\|---\| \| 0 \| No changes will be applied. \| \| 1 \| Only price changes will be applied. \| \| 2 \| All changes will be applied. \| |
