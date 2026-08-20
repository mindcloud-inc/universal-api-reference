# Centerpoint: Get Product



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-product?connectionId=$CONNECTION_ID&PRODUCT_ID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "PRODUCT_ID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-product?${params}`, {
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
| `PRODUCT_ID` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[productions]` | string | no |  |
| `fields[products]` | string | no |  |
| `fields[properties]` | string | no |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "accountId": 1,
        "approvedAt": {},
        "budgetedAt": {},
        "buildingDivisionId": 1,
        "completedAt": {},
        "corrected": "string",
        "correctedAt": "string",
        "correction": "string",
        "cost": 1,
        "createdAt": "string",
        "deletedAt": {},
        "description": "string",
        "fileId": 1,
        "hideFromInvoice": 1,
        "isBudgeted": true,
        "isCorrected": true,
        "locations": [
          [
            "string"
          ]
        ],
        "locationsLatLong": [
          {}
        ],
        "name": "Ava Chen",
        "pinAerialId": {},
        "pinLocations": {},
        "price": 1,
        "priority": 1,
        "productTemplateId": 1,
        "quantity": 1,
        "unitCost": 1,
        "unitPrice": 1,
        "units": "string",
        "updatedAt": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.accountId` | number |  |
| `attributes.approvedAt` | object |  |
| `attributes.budgetedAt` | object |  |
| `attributes.buildingDivisionId` | number |  |
| `attributes.completedAt` | object |  |
| `attributes.corrected` | string |  |
| `attributes.correctedAt` | string |  |
| `attributes.correction` | string |  |
| `attributes.cost` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.description` | string |  |
| `attributes.fileId` | number |  |
| `attributes.hideFromInvoice` | number |  |
| `attributes.isBudgeted` | boolean |  |
| `attributes.isCorrected` | boolean |  |
| `attributes.locations` | array<array> |  |
| `attributes.locationsLatLong` | array<object> |  |
| `attributes.name` | string |  |
| `attributes.pinAerialId` | object |  |
| `attributes.pinLocations` | object |  |
| `attributes.price` | number |  |
| `attributes.priority` | number |  |
| `attributes.productTemplateId` | number |  |
| `attributes.quantity` | number |  |
| `attributes.unitCost` | number |  |
| `attributes.unitPrice` | number |  |
| `attributes.units` | string |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET products/:PRODUCT_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

