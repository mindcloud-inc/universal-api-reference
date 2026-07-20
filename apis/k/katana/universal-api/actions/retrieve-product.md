# Katana: Retrieve Product

Retrieves a product by ID from Katana.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-product?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-product?${params}`, {
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
| `id` | number | yes | Product id |
| `extend[]` | array<string> | no | Array of objects that need to be added to the response |

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
      "isAutoAssembly": true,
      "isProducible": true,
      "isPurchasable": true,
      "isSellable": true,
      "name": "Ava Chen",
      "operationsInSequence": true,
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
| `isAutoAssembly` | boolean |  |
| `isProducible` | boolean |  |
| `isPurchasable` | boolean |  |
| `isSellable` | boolean |  |
| `name` | string |  |
| `operationsInSequence` | boolean |  |
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
| `variants[].id` | number |  |
| `variants[].internalBarcode` | string |  |
| `variants[].leadTime` | number |  |
| `variants[].minimumOrderQuantity` | number |  |
| `variants[].productId` | number |  |
| `variants[].purchasePrice` | number |  |
| `variants[].registeredBarcode` | string |  |
| `variants[].salesPrice` | number |  |
| `variants[].sku` | string |  |
| `variants[].supplierItemCodes` | array<string> |  |
| `variants[].type` | string |  |
| `variants[].updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `GET /products/:id` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-product.md) for the provider-specific parameters and requirements.

