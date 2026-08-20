# Centerpoint: Get Building Division



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building-division
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building-division?connectionId=$CONNECTION_ID&BUILDING_DIVISIONS_ID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "BUILDING_DIVISIONS_ID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-building-division?${params}`, {
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
| `BUILDING_DIVISIONS_ID` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[products]` | string | no |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "approvedReplaceBudget": {},
        "averageWallHeight": 1,
        "budgetImportance": {},
        "buildingId": 1,
        "createdAt": "string",
        "deletedAt": {},
        "importId": {},
        "installYear": 1,
        "measurement": 1,
        "name": "Ava Chen",
        "pitchRise": 1,
        "recommendation": "string",
        "replaceBudget": 1,
        "replacementBudgetedAt": {},
        "replacePrice": 1,
        "replaceUnitPrice": 1,
        "replaceYear": 1,
        "score": 1,
        "updatedAt": "string"
      },
      "id": "string",
      "relationships": {
        "outlines": {
          "data": [
            {}
          ]
        },
        "products": {
          "data": [
            {}
          ]
        },
        "productTemplateTag": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "scores": {
          "data": [
            {}
          ]
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.approvedReplaceBudget` | object |  |
| `attributes.averageWallHeight` | number |  |
| `attributes.budgetImportance` | object |  |
| `attributes.buildingId` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.importId` | object |  |
| `attributes.installYear` | number |  |
| `attributes.measurement` | number |  |
| `attributes.name` | string |  |
| `attributes.pitchRise` | number |  |
| `attributes.recommendation` | string |  |
| `attributes.replaceBudget` | number |  |
| `attributes.replacementBudgetedAt` | object |  |
| `attributes.replacePrice` | number |  |
| `attributes.replaceUnitPrice` | number |  |
| `attributes.replaceYear` | number |  |
| `attributes.score` | number |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `relationships.outlines.data` | array<object> |  |
| `relationships.products.data` | array<object> |  |
| `relationships.productTemplateTag.data.id` | string |  |
| `relationships.productTemplateTag.data.type` | string |  |
| `relationships.scores.data` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET building_divisions/:BUILDING_DIVISIONS_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-building-division.md) for the provider-specific parameters and requirements.

