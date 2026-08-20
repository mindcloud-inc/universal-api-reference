# Centerpoint: List Production Items



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-production-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-production-items?connectionId=$CONNECTION_ID&limit=25&offset=0&PRODUCTION_ID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "PRODUCTION_ID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-production-items?${params}`, {
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
| `filter[domain]` | string | no | Example: `production`. |
| `filter[production]` | string | no | Example: `1882222`. |
| `sort` | string | no | Example: `type`. |
| `PRODUCTION_ID` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reports[0]` | string | no |  |
| `reports[1]` | string | no |  |
| `reports[2]` | string | no |  |
| `reports[3]` | string | no |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "cost": 1,
        "createdAt": "string",
        "deletedAt": {},
        "isTaxable": true,
        "materialId": {},
        "name": "Ava Chen",
        "quantity": 1,
        "type": "string",
        "unitCost": 1,
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
| `attributes.cost` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.isTaxable` | boolean |  |
| `attributes.materialId` | object |  |
| `attributes.name` | string |  |
| `attributes.quantity` | number |  |
| `attributes.type` | string |  |
| `attributes.unitCost` | number |  |
| `attributes.units` | string |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET production_items` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-production-items.md) for the provider-specific parameters and requirements.

