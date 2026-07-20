# Fiddle: List Inventory Types

Retrieves inventory type records from Fiddle.

```
GET https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-types?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountingCategory": "string",
      "billOfMaterialDefaultMeasurementUnit": {},
      "billOfMaterialDefaultMeasurementUnitId": {},
      "billOfMaterialType": {},
      "changeable": true,
      "createdAt": "string",
      "defaultMeasurementUnit": {
        "abbreviation": "string",
        "description": "string",
        "id": "string",
        "name": "Ava Chen",
        "unitType": "string"
      },
      "defaultMeasurementUnitId": "string",
      "description": "string",
      "hasBillOfMaterial": true,
      "hasFormula": true,
      "id": "string",
      "name": "Ava Chen",
      "prefix": "string",
      "recordType": {},
      "recordTypeId": {},
      "sortIndex": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `accountingCategory` | string |  |
| `billOfMaterialDefaultMeasurementUnit` | object |  |
| `billOfMaterialDefaultMeasurementUnitId` | object |  |
| `billOfMaterialType` | object |  |
| `changeable` | boolean |  |
| `createdAt` | string |  |
| `defaultMeasurementUnit.abbreviation` | string |  |
| `defaultMeasurementUnit.description` | string |  |
| `defaultMeasurementUnit.id` | string |  |
| `defaultMeasurementUnit.name` | string |  |
| `defaultMeasurementUnit.unitType` | string |  |
| `defaultMeasurementUnitId` | string |  |
| `description` | string |  |
| `hasBillOfMaterial` | boolean |  |
| `hasFormula` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `prefix` | string |  |
| `recordType` | object |  |
| `recordTypeId` | object |  |
| `sortIndex` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Fiddle API, this operation is `GET /inventory-types` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inventory-types.md) for the provider-specific parameters and requirements.

