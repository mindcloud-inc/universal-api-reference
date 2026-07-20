# Katana: Update Material

Updates an existing material in Katana.

```
PUT https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-material
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-material" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-material', {
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
| `id` | number | yes | Material id |
| `name` | string | no |  |
| `uom` | string | no |  |
| `categoryName` | string | no |  |
| `defaultSupplierId` | number | no |  |
| `additionalInfo` | string | no |  |
| `batchTracked` | boolean | no |  |
| `isSellable` | boolean | no |  |
| `isArchived` | boolean | no |  |
| `purchaseUom` | string | no | If used, then purchase_uom_conversion_rate must have a value as well. |
| `purchaseUomConversionRate` | number | no | If used, then purchase_uom must have a value as well. |
| `configs[]` | array<object> | no | When updating configs, all configs and values must be provided. Existing ones are matched, new ones are created, and configs not provided in the update are deleted. |
| `configs[].id` | number | no | If config ID is used to map the config, then name is ignored. |
| `configs[].name` | string | no | If config name is used to map the config, then we match to the existing config by name. If a match is not found, a new one is created. |
| `configs[].values[]` | array<string> | no |  |
| `customFieldCollectionId` | number | no |  |

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
| `variants[].id` | number |  |
| `variants[].internalBarcode` | string |  |
| `variants[].leadTime` | number |  |
| `variants[].minimumOrderQuantity` | number |  |
| `variants[].productId` | number |  |
| `variants[].purchasePrice` | number |  |
| `variants[].registeredBarcode` | string |  |
| `variants[].salesPrice` | string |  |
| `variants[].sku` | string |  |
| `variants[].supplierItemCodes` | array<string> |  |
| `variants[].type` | string |  |
| `variants[].updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `PATCH /materials/:id` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-material.md) for the provider-specific parameters and requirements.

