# Katana: Retrieve Variant

Retrieves a variant by ID from Katana.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-variant?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-variant?${params}`, {
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
| `id` | number | yes | Variant id |
| `extend[]` | array<string> | no | Array of objects that need to be added to the response |

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

Through the native Katana API, this operation is `GET /variants/:id` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-variant.md) for the provider-specific parameters and requirements.

