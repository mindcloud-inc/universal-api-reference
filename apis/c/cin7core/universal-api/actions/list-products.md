# Cin7 Core: List Products



```
GET https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cin7 Core `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/list-products?${params}`, {
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
| `ID` | string | no | Returns stock info of a particular product (Default: null) |
| `Name` | string | no | Only return products with product name containing specified name value (Default: null) |
| `Sku` | string | no | Only return products with product sku containing specified sku value (Default: null) |
| `ModifiedSince` | date | no | Only return Products modified since specified date (UTC time) in ISO 8601 format. (Default: null) |
| `IncludeDeprecated` | boolean | no | Returns all Products, including deprecated, if set to true. If set to false or if it is not specified then returns only active (ie. non-deprecated) Products (Default: false) |
| `IncludeBOM` | boolean | no | Include Bill Of Materials information (Default: false) |
| `IncludeSuppliers` | boolean | no | Include Suppliers information (Default: false) |
| `IncludeMovements` | boolean | no | Include Movements information (Default: false) |
| `IncludeAttachments` | boolean | no | Include Attachments information (Default: false) |
| `IncludeReorderLevels` | boolean | no | Include Reorder Levels information (Default: false) |
| `IncludeCustomPrices` | boolean | no | Include Customer specific Prices (Default: false) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Products": {
        "AdditionalAttribute1": "string",
        "AdditionalAttribute10": "string",
        "AdditionalAttribute2": "string",
        "AdditionalAttribute3": "string",
        "AdditionalAttribute4": "string",
        "AdditionalAttribute5": "string",
        "AdditionalAttribute6": "string",
        "AdditionalAttribute7": "string",
        "AdditionalAttribute8": "string",
        "AdditionalAttribute9": "string",
        "AssemblyCostEstimationMethod": "string",
        "AssemblyInstructionURL": "https://example.com",
        "Attachments": [
          "string"
        ],
        "AttributeSet": "string",
        "AutoAssembly": "string",
        "AutoDisassembly": "string",
        "AverageCost": "string",
        "Barcode": "string",
        "BillOfMaterial": "string",
        "BillOfMaterialsProducts": [
          "string"
        ],
        "BillOfMaterialsServices": [
          "string"
        ],
        "BOMType": "string",
        "Brand": "string",
        "CartonHeight": "string",
        "CartonInnerQuantity": "string",
        "CartonLength": "string",
        "CartonQuantity": "string",
        "CartonWidth": "string",
        "Category": "string",
        "COGSAccount": "string",
        "CostingMethod": "string",
        "CountryOfOrigin": "string",
        "CountryOfOriginCode": "string",
        "CustomPrices": [
          "string"
        ],
        "DefaultLocation": "string",
        "Description": "string",
        "DimensionsUnits": "string",
        "DiscountRule": "string",
        "DropShipMode": "string",
        "ExpenseAccount": "string",
        "Height": "string",
        "HSCode": "string",
        "ID": "string",
        "InternalNote": "string",
        "InventoryAccount": "string",
        "LastModifiedOn": "string",
        "Length": "string",
        "MinimumBeforeReorder": "string",
        "Movements": [
          "string"
        ],
        "Name": "Ava Chen",
        "PickZones": "string",
        "PriceTier1": "string",
        "PriceTier10": "string",
        "PriceTier2": "string",
        "PriceTier3": "string",
        "PriceTier4": "string",
        "PriceTier5": "string",
        "PriceTier6": "string",
        "PriceTier7": "string",
        "PriceTier8": "string",
        "PriceTier9": "string",
        "PriceTiers": {
          "Tier 1": "string",
          "Tier 10": "string",
          "Tier 2": "string",
          "Tier 3": "string",
          "Tier 4": "string",
          "Tier 5": "string",
          "Tier 6": "string",
          "Tier 7": "string",
          "Tier 8": "string",
          "Tier 9": "string"
        },
        "PurchaseTaxRule": "string",
        "QuantityToProduce": "string",
        "ReorderLevels": [
          "string"
        ],
        "ReorderQuantity": "string",
        "RevenueAccount": "string",
        "SaleTaxRule": "string",
        "Sellable": "string",
        "ShortDescription": "string",
        "SKU": "string",
        "Status": "string",
        "StockLocator": "string",
        "Suppliers": [
          "string"
        ],
        "Tags": "string",
        "Type": "string",
        "UOM": "string",
        "Weight": "string",
        "WeightUnits": "string",
        "Width": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Products` | array |  |
| `Products.AdditionalAttribute1` | string |  |
| `Products.AdditionalAttribute10` | string |  |
| `Products.AdditionalAttribute2` | string |  |
| `Products.AdditionalAttribute3` | string |  |
| `Products.AdditionalAttribute4` | string |  |
| `Products.AdditionalAttribute5` | string |  |
| `Products.AdditionalAttribute6` | string |  |
| `Products.AdditionalAttribute7` | string |  |
| `Products.AdditionalAttribute8` | string |  |
| `Products.AdditionalAttribute9` | string |  |
| `Products.AssemblyCostEstimationMethod` | string |  |
| `Products.AssemblyInstructionURL` | string |  |
| `Products.Attachments` | array |  |
| `Products.AttributeSet` | string |  |
| `Products.AutoAssembly` | string |  |
| `Products.AutoDisassembly` | string |  |
| `Products.AverageCost` | string |  |
| `Products.Barcode` | string |  |
| `Products.BillOfMaterial` | string |  |
| `Products.BillOfMaterialsProducts` | array |  |
| `Products.BillOfMaterialsServices` | array |  |
| `Products.BOMType` | string |  |
| `Products.Brand` | string |  |
| `Products.CartonHeight` | string |  |
| `Products.CartonInnerQuantity` | string |  |
| `Products.CartonLength` | string |  |
| `Products.CartonQuantity` | string |  |
| `Products.CartonWidth` | string |  |
| `Products.Category` | string |  |
| `Products.COGSAccount` | string |  |
| `Products.CostingMethod` | string |  |
| `Products.CountryOfOrigin` | string |  |
| `Products.CountryOfOriginCode` | string |  |
| `Products.CustomPrices` | array |  |
| `Products.DefaultLocation` | string |  |
| `Products.Description` | string |  |
| `Products.DimensionsUnits` | string |  |
| `Products.DiscountRule` | string |  |
| `Products.DropShipMode` | string |  |
| `Products.ExpenseAccount` | string |  |
| `Products.Height` | string |  |
| `Products.HSCode` | string |  |
| `Products.ID` | string |  |
| `Products.InternalNote` | string |  |
| `Products.InventoryAccount` | string |  |
| `Products.LastModifiedOn` | string |  |
| `Products.Length` | string |  |
| `Products.MinimumBeforeReorder` | string |  |
| `Products.Movements` | array |  |
| `Products.Name` | string |  |
| `Products.PickZones` | string |  |
| `Products.PriceTier1` | string |  |
| `Products.PriceTier10` | string |  |
| `Products.PriceTier2` | string |  |
| `Products.PriceTier3` | string |  |
| `Products.PriceTier4` | string |  |
| `Products.PriceTier5` | string |  |
| `Products.PriceTier6` | string |  |
| `Products.PriceTier7` | string |  |
| `Products.PriceTier8` | string |  |
| `Products.PriceTier9` | string |  |
| `Products.PriceTiers` | object |  |
| `Products.PriceTiers.Tier 1` | string |  |
| `Products.PriceTiers.Tier 10` | string |  |
| `Products.PriceTiers.Tier 2` | string |  |
| `Products.PriceTiers.Tier 3` | string |  |
| `Products.PriceTiers.Tier 4` | string |  |
| `Products.PriceTiers.Tier 5` | string |  |
| `Products.PriceTiers.Tier 6` | string |  |
| `Products.PriceTiers.Tier 7` | string |  |
| `Products.PriceTiers.Tier 8` | string |  |
| `Products.PriceTiers.Tier 9` | string |  |
| `Products.PurchaseTaxRule` | string |  |
| `Products.QuantityToProduce` | string |  |
| `Products.ReorderLevels` | array |  |
| `Products.ReorderQuantity` | string |  |
| `Products.RevenueAccount` | string |  |
| `Products.SaleTaxRule` | string |  |
| `Products.Sellable` | string |  |
| `Products.ShortDescription` | string |  |
| `Products.SKU` | string |  |
| `Products.Status` | string |  |
| `Products.StockLocator` | string |  |
| `Products.Suppliers` | array |  |
| `Products.Tags` | string |  |
| `Products.Type` | string |  |
| `Products.UOM` | string |  |
| `Products.Weight` | string |  |
| `Products.WeightUnits` | string |  |
| `Products.Width` | string |  |

## Native endpoint

Through the native Cin7 Core API, this operation is `GET product` (base URL `https://inventory.dearsystems.com/externalapi/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

