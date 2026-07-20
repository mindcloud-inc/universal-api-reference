# Alto: Filter Inventory

Finds inventory items in Alto by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/filter-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/filter-inventory?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/filter-inventory?${params}`, {
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
| `categoryType` | string | no | Inventory category type filter. |
| `inventoryStatus` | string | no | Inventory status filter. |
| `recordType` | string | no | Inventory record type filter. |
| `branchIds` | string | no | One or more Alto branch IDs to filter inventory results. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "branchId": "string",
      "instructionDate": "2026-05-07T12:00:00.000Z",
      "inventoryId": "string",
      "recordType": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `branchId` | string |  |
| `instructionDate` | date |  |
| `inventoryId` | string |  |
| `recordType` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /inventory/filter` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/filter-inventory.md) for the provider-specific parameters and requirements.

