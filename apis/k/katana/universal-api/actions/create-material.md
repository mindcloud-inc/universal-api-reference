# Katana: Create Material

Creates a new material in Katana.

```
POST https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-material
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-material" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "variants[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-material', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "variants[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `uom` | string | no |  |
| `categoryName` | string | no |  |
| `defaultSupplierId` | number | no |  |
| `additionalInfo` | string | no |  |
| `batchTracked` | boolean | no |  |
| `isSellable` | boolean | no |  |
| `purchaseUom` | string | no |  |
| `purchaseUomConversionRate` | number | no |  |
| `configs[]` | array<object> | no |  |
| `configs[].name` | string | no |  |
| `configs[].values[]` | array<string> | no |  |
| `customFieldCollectionId` | number | no |  |
| `variants[]` | array<object> | yes |  |
| `variants[].sku` | string | no |  |
| `variants[].purchasePrice` | number | no |  |
| `variants[].internalBarcode` | string | no |  |
| `variants[].registeredBarcode` | string | no |  |
| `variants[].supplierItemCodes[]` | array<string> | no |  |
| `variants[].leadTime` | number | no |  |
| `variants[].minimumOrderQuantity` | number | no |  |
| `variants[].configAttributes[]` | array<object> | no |  |
| `variants[].configAttributes[].configName` | string | no |  |
| `variants[].configAttributes[].configValue` | string | no |  |
| `variants[].customFields[]` | array<object> | no |  |
| `variants[].customFields[].fieldName` | string | no |  |
| `variants[].customFields[].fieldValue` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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

Through the native Katana API, this operation is `POST /materials` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-material.md) for the provider-specific parameters and requirements.

