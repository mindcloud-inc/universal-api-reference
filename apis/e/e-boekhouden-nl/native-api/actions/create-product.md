# Create Product with e-Boekhouden.nl

Creates a new product in e-Boekhouden.nl.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/product`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [Create Product](https://api.e-boekhouden.nl/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | The code of the product. Error codes ART_004 Product Code is missing. ART_007 Product Code is too long. Maximum length: 20. |
| `description` | body | `string` | yes | The description of the product. Error codes ART_005 Product Description is missing. Maximum length: 35000. |
| `unitId` | body | `number` | no | The unit ID of the product. Error codes ART_011 Product Unit could not be found. |
| `active` | body | `boolean` | no | Whether the product is active. |
| `groupId` | body | `number` | no | The group ID of the product. Error codes ART_012 Product Group could not be found. |
| `purchasePriceExcl` | body | `number` | no | The purchase price (excluding VAT) of the product. Error codes ART_027 The value of PurchasePriceExcl exceeds the maximum value of 999999999999.00. ART_032 The value of PurchasePriceExcl is below the minimum value of -999999999999.00. |
| `priceExcl` | body | `number` | no | The price (excluding VAT) of the product. This field can not be combined with `priceIncl`. Error codes ART_018 Either priceExcl or priceIncl is required. ART_019 Both priceExcl and priceIncl are required with current VAT code. ART_024 The value of PriceExcl exceeds the maximum value of 999999999999.00. ART_026 The value of PriceIncl after applying VAT exceeds the maximum value of 999999999999.00. ART_029 The value of PriceExcl is below the minimum value of -999999999999.00. ART_031 The value of PriceIncl after applying VAT is below the minimum value of -999999999999.00. |
| `priceIncl` | body | `number` | no | The price (including VAT) of the product. This field can not be combined with `priceExcl`. Error codes ART_016 priceIncl cannot have a value when priceExcl is passed. ART_018 Either priceExcl or priceIncl is required. ART_019 Both priceExcl and priceIncl are required with current VAT code. ART_025 The value of PriceIncl exceeds the maximum value of 999999999999.00. ART_030 The value of PriceIncl is below the minimum value of -999999999999.00. |
| `vat` | body | `string` | yes | The VAT code of the product. Only supports VAT codes of type 'Sale'. Error codes ART_013 Product VAT code could not be found. ART_017 Product VAT code is required. |
| `ledgerId` | body | `number` | yes | The ledger ID of the product. Error codes ART_006 Product Ledger ID is missing. ART_009 Product Ledger could not be found. ART_028 Ledger category must be 'BAL' or 'VW'. |
| `costCenterId` | body | `number` | no | The cost center ID of the product. Error codes ART_010 Product Cost center is inactive. ART_015 Product cost center could not be found. |
| `inStockManagement` | body | `boolean` | no | Whether the product will be Included in automatic inventory management. |
