# Katana: List Variants

Lists variants in your Katana account.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-variants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-variants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-variants?${params}`, {
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
| `ids[]` | array<number> | no | Filters variants by an array of IDs |
| `productId` | number | no | Filters variants by a product id |
| `materialId` | number | no | Filters variants by a material id |
| `sku[]` | array<string> | no | Filters variants by skus |
| `salesPrice` | number | no | Filters variants by a sales price |
| `purchasePrice` | number | no | Filters variants by a purchase price |
| `internalBarcode` | string | no | Filters variants by an internal barcode |
| `registeredBarcode` | string | no | Filters variants by a registered barcode |
| `supplierItemCodes[]` | array<string> | no | Filters variants by supplier item codes. Returns the variants that match with any of the codes in the array. |
| `extend[]` | array<string> | no | Array of objects that need to be added to the response |
| `includeDeleted` | boolean | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `includeArchived` | boolean | no | Archived data is excluded from result set by default. Set to true to include it. |
| `createdAtMin` | string | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `createdAtMax` | string | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updatedAtMin` | string | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updatedAtMax` | string | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configAttributes": [
        {
          "configName": "Ava Chen",
          "configValue": "string"
        }
      ],
      "createdAt": "string",
      "deletedAt": "string",
      "id": 1,
      "internalBarcode": "string",
      "materialId": "string",
      "productId": 1,
      "productOrMaterial": {
        "additionalInfo": "string",
        "batchTracked": true,
        "categoryName": "Ava Chen",
        "configs": [
          {
            "id": 1,
            "name": "Ava Chen",
            "productId": 1,
            "values": [
              "string"
            ]
          }
        ],
        "createdAt": "string",
        "defaultSupplierId": 1,
        "id": 1,
        "isProducible": true,
        "isPurchasable": true,
        "name": "Ava Chen",
        "purchaseUom": "string",
        "purchaseUomConversionRate": 1,
        "type": "string",
        "uom": "string",
        "updatedAt": "string",
        "variants": [
          {
            "configAttributes": [
              {
                "configName": "Ava Chen",
                "configValue": "string"
              }
            ],
            "createdAt": "string",
            "customFields": [
              {
                "fieldName": "Ava Chen",
                "fieldValue": "string"
              }
            ],
            "id": 1,
            "internalBarcode": "string",
            "leadTime": 1,
            "minimumOrderQuantity": 1,
            "productId": 1,
            "purchasePrice": 1,
            "registeredBarcode": "string",
            "salesPrice": 1,
            "sku": "string",
            "supplierItemCodes": [
              "string"
            ],
            "type": "string",
            "updatedAt": "string"
          }
        ]
      },
      "purchasePrice": 1,
      "registeredBarcode": "string",
      "salesPrice": 1,
      "sku": "string",
      "supplierItemCodes": [
        "string"
      ],
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configAttributes` | array<object> |  |
| `configAttributes[].configName` | string |  |
| `configAttributes[].configValue` | string |  |
| `createdAt` | string |  |
| `deletedAt` | string |  |
| `id` | number |  |
| `internalBarcode` | string |  |
| `materialId` | string |  |
| `productId` | number |  |
| `productOrMaterial` | object |  |
| `productOrMaterial.additionalInfo` | string |  |
| `productOrMaterial.batchTracked` | boolean |  |
| `productOrMaterial.categoryName` | string |  |
| `productOrMaterial.configs` | array<object> |  |
| `productOrMaterial.configs[].id` | number |  |
| `productOrMaterial.configs[].name` | string |  |
| `productOrMaterial.configs[].productId` | number |  |
| `productOrMaterial.configs[].values` | array<string> |  |
| `productOrMaterial.createdAt` | string |  |
| `productOrMaterial.defaultSupplierId` | number |  |
| `productOrMaterial.id` | number |  |
| `productOrMaterial.isProducible` | boolean |  |
| `productOrMaterial.isPurchasable` | boolean |  |
| `productOrMaterial.name` | string |  |
| `productOrMaterial.purchaseUom` | string |  |
| `productOrMaterial.purchaseUomConversionRate` | number |  |
| `productOrMaterial.type` | string |  |
| `productOrMaterial.uom` | string |  |
| `productOrMaterial.updatedAt` | string |  |
| `productOrMaterial.variants` | array<object> |  |
| `productOrMaterial.variants[].configAttributes` | array<object> |  |
| `productOrMaterial.variants[].configAttributes[].configName` | string |  |
| `productOrMaterial.variants[].configAttributes[].configValue` | string |  |
| `productOrMaterial.variants[].createdAt` | string |  |
| `productOrMaterial.variants[].customFields` | array<object> |  |
| `productOrMaterial.variants[].customFields[].fieldName` | string |  |
| `productOrMaterial.variants[].customFields[].fieldValue` | string |  |
| `productOrMaterial.variants[].id` | number |  |
| `productOrMaterial.variants[].internalBarcode` | string |  |
| `productOrMaterial.variants[].leadTime` | number |  |
| `productOrMaterial.variants[].minimumOrderQuantity` | number |  |
| `productOrMaterial.variants[].productId` | number |  |
| `productOrMaterial.variants[].purchasePrice` | number |  |
| `productOrMaterial.variants[].registeredBarcode` | string |  |
| `productOrMaterial.variants[].salesPrice` | number |  |
| `productOrMaterial.variants[].sku` | string |  |
| `productOrMaterial.variants[].supplierItemCodes` | array<string> |  |
| `productOrMaterial.variants[].type` | string |  |
| `productOrMaterial.variants[].updatedAt` | string |  |
| `purchasePrice` | number |  |
| `registeredBarcode` | string |  |
| `salesPrice` | number |  |
| `sku` | string |  |
| `supplierItemCodes` | array<string> |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `GET /variants` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-variants.md) for the provider-specific parameters and requirements.

