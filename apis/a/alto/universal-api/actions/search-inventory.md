# Alto: Search Inventory

Finds inventory items in Alto by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/search-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/search-inventory?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/search-inventory?${params}`, {
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
| `query` | string | yes | Search text for inventory items. |
| `recordType` | string | no | Inventory record type filter. |
| `archived` | boolean | no | Whether to search archived inventory records. |

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

Through the native Alto API, this operation is `GET /inventory/search` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-inventory.md) for the provider-specific parameters and requirements.

