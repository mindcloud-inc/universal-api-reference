# Katana: List Current Inventory

Lists current inventory records in Katana.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-current-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-current-inventory?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-current-inventory?${params}`, {
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
| `locationId` | number | no | Filters inventories by a valid location id |
| `variantId[]` | array<number> | no | Filters inventories by valid variant ids |
| `includeArchived` | boolean | no | Includes archived inventories |
| `extend[]` | array<string> | no | Array of objects that need to be added to the response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "averageCost": "string",
      "location": {
        "address": {
          "city": "string",
          "country": "string",
          "id": 1,
          "line1": "string",
          "line2": "string",
          "state": "string",
          "zip": "string"
        },
        "addressId": 1,
        "createdAt": "string",
        "id": 1,
        "isPrimary": true,
        "legalName": "Ava Chen",
        "manufacturingAllowed": true,
        "name": "Ava Chen",
        "salesAllowed": true,
        "updatedAt": "string"
      },
      "locationId": 1,
      "quantityCommitted": "string",
      "quantityExpected": "string",
      "quantityInStock": "string",
      "quantityMissingOrExcess": "string",
      "quantityPotential": "string",
      "reorderPoint": "string",
      "valueInStock": "string",
      "variant": {
        "configAttributes": [
          {
            "configName": "Ava Chen",
            "configValue": "string"
          }
        ],
        "createdAt": "string",
        "id": 1,
        "internalBarcode": "string",
        "productId": 1,
        "productOrMaterialName": "Ava Chen",
        "purchasePrice": 1,
        "registeredBarcode": "string",
        "salesPrice": 1,
        "sku": "string",
        "supplierItemCodes": [
          "string"
        ],
        "type": "string",
        "updatedAt": "string"
      },
      "variantId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageCost` | string |  |
| `location` | object |  |
| `location.address` | object |  |
| `location.address.city` | string |  |
| `location.address.country` | string |  |
| `location.address.id` | number |  |
| `location.address.line1` | string |  |
| `location.address.line2` | string |  |
| `location.address.state` | string |  |
| `location.address.zip` | string |  |
| `location.addressId` | number |  |
| `location.createdAt` | string |  |
| `location.id` | number |  |
| `location.isPrimary` | boolean |  |
| `location.legalName` | string |  |
| `location.manufacturingAllowed` | boolean |  |
| `location.name` | string |  |
| `location.salesAllowed` | boolean |  |
| `location.updatedAt` | string |  |
| `locationId` | number |  |
| `quantityCommitted` | string |  |
| `quantityExpected` | string |  |
| `quantityInStock` | string |  |
| `quantityMissingOrExcess` | string |  |
| `quantityPotential` | string |  |
| `reorderPoint` | string |  |
| `valueInStock` | string |  |
| `variant` | object |  |
| `variant.configAttributes` | array<object> |  |
| `variant.configAttributes[].configName` | string |  |
| `variant.configAttributes[].configValue` | string |  |
| `variant.createdAt` | string |  |
| `variant.id` | number |  |
| `variant.internalBarcode` | string |  |
| `variant.productId` | number |  |
| `variant.productOrMaterialName` | string |  |
| `variant.purchasePrice` | number |  |
| `variant.registeredBarcode` | string |  |
| `variant.salesPrice` | number |  |
| `variant.sku` | string |  |
| `variant.supplierItemCodes` | array<string> |  |
| `variant.type` | string |  |
| `variant.updatedAt` | string |  |
| `variantId` | number |  |

## Native endpoint

Through the native Katana API, this operation is `GET /inventory` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-current-inventory.md) for the provider-specific parameters and requirements.

