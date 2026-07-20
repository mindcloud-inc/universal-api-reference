# Katana: List Materials

Lists materials in your Katana account.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-materials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-materials?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-materials?${params}`, {
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
| `ids[]` | array<number> | no | Filters materials by an array of IDs |
| `name` | string | no | Filters materials by a name |
| `uom` | string | no | Filters materials by a uom |
| `defaultSupplierId` | number | no | Filters materials by a default_supplier_id |
| `isSellable` | boolean | no | Filters materials by a is_sellable |
| `batchTracked` | boolean | no | Filters materials by a batch_tracked |
| `purchaseUom` | string | no | Filters materials by a purchase_uom |
| `purchaseUomConversionRate` | number | no | Filters materials by a purchase_uom_conversion_rate |
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
      "additionalInfo": "string",
      "archivedAt": "string",
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
      "customFieldCollectionId": 1,
      "defaultSupplierId": 1,
      "id": 1,
      "isSellable": true,
      "name": "Ava Chen",
      "purchaseUom": "string",
      "purchaseUomConversionRate": 1,
      "supplier": {
        "comment": "string",
        "createdAt": "string",
        "currency": "string",
        "deletedAt": "string",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "updatedAt": "string"
      },
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
          "deletedAt": "string",
          "id": 1,
          "internalBarcode": "string",
          "leadTime": 1,
          "materialId": 1,
          "minimumOrderQuantity": 1,
          "productId": "string",
          "purchasePrice": 1,
          "registeredBarcode": "string",
          "salesPrice": "string",
          "sku": "string",
          "supplierItemCodes": [
            "string"
          ],
          "type": "string",
          "updatedAt": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalInfo` | string |  |
| `archivedAt` | string |  |
| `batchTracked` | boolean |  |
| `categoryName` | string |  |
| `configs` | array<object> |  |
| `configs[].id` | number |  |
| `configs[].name` | string |  |
| `configs[].productId` | number |  |
| `configs[].values` | array<string> |  |
| `createdAt` | string |  |
| `customFieldCollectionId` | number |  |
| `defaultSupplierId` | number |  |
| `id` | number |  |
| `isSellable` | boolean |  |
| `name` | string |  |
| `purchaseUom` | string |  |
| `purchaseUomConversionRate` | number |  |
| `supplier` | object |  |
| `supplier.comment` | string |  |
| `supplier.createdAt` | string |  |
| `supplier.currency` | string |  |
| `supplier.deletedAt` | string |  |
| `supplier.email` | string |  |
| `supplier.id` | number |  |
| `supplier.name` | string |  |
| `supplier.updatedAt` | string |  |
| `type` | string |  |
| `uom` | string |  |
| `updatedAt` | string |  |
| `variants` | array<object> |  |
| `variants[].configAttributes` | array<object> |  |
| `variants[].configAttributes[].configName` | string |  |
| `variants[].configAttributes[].configValue` | string |  |
| `variants[].createdAt` | string |  |
| `variants[].customFields` | array<object> |  |
| `variants[].customFields[].fieldName` | string |  |
| `variants[].customFields[].fieldValue` | string |  |
| `variants[].deletedAt` | string |  |
| `variants[].id` | number |  |
| `variants[].internalBarcode` | string |  |
| `variants[].leadTime` | number |  |
| `variants[].materialId` | number |  |
| `variants[].minimumOrderQuantity` | number |  |
| `variants[].productId` | string |  |
| `variants[].purchasePrice` | number |  |
| `variants[].registeredBarcode` | string |  |
| `variants[].salesPrice` | string |  |
| `variants[].sku` | string |  |
| `variants[].supplierItemCodes` | array<string> |  |
| `variants[].type` | string |  |
| `variants[].updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `GET /materials` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-materials.md) for the provider-specific parameters and requirements.

