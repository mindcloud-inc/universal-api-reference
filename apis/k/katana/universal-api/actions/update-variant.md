# Katana: Update Variant

Updates an existing variant in Katana.

```
PUT https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-variant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-variant', {
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
| `id` | number | yes | Variant id |
| `sku` | string | no |  |
| `salesPrice` | number | no |  |
| `purchasePrice` | number | no |  |
| `productId` | number | no |  |
| `supplierItemCodes[]` | array<string> | no |  |
| `internalBarcode` | string | no |  |
| `registeredBarcode` | string | no |  |
| `materialId` | number | no |  |
| `leadTime` | number | no |  |
| `minimumOrderQuantity` | number | no |  |
| `configAttributes[]` | array<object> | no |  |
| `configAttributes[].configName` | string | no | If a matching config name is not found, an error is returned. Use the product/material endpoint to update the configs. |
| `configAttributes[].configValue` | string | no | If a matching config name is not found, the product/material config list of values is updated, and a new value is added. |
| `customFields[]` | array<object> | no |  |
| `customFields[].fieldName` | string | no |  |
| `customFields[].fieldValue` | string | no |  |

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
      "customFields": [
        {
          "fieldName": "Ava Chen",
          "fieldValue": "string"
        }
      ],
      "id": 1,
      "internalBarcode": "string",
      "leadTime": 1,
      "materialId": "string",
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
| `customFields` | array<object> |  |
| `customFields[].fieldName` | string |  |
| `customFields[].fieldValue` | string |  |
| `id` | number |  |
| `internalBarcode` | string |  |
| `leadTime` | number |  |
| `materialId` | string |  |
| `minimumOrderQuantity` | number |  |
| `productId` | number |  |
| `purchasePrice` | number |  |
| `registeredBarcode` | string |  |
| `salesPrice` | number |  |
| `sku` | string |  |
| `supplierItemCodes` | array<string> |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `PATCH /variants/:id` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-variant.md) for the provider-specific parameters and requirements.

