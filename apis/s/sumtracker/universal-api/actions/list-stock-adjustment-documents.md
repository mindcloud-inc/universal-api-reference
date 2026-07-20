# Sumtracker: List Stock Adjustment Documents

Retrieves stock adjustment documents from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-stock-adjustment-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-stock-adjustment-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-stock-adjustment-documents?${params}`, {
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
| `adjustment_type` | string | no |  |
| `created_range_after` | date | no |  |
| `created_range_before` | date | no |  |
| `is_complete` | boolean | no |  |
| `is_task_in_progress` | boolean | no |  |
| `limit` | number | no |  |
| `notes` | string | no |  |
| `number` | string | no |  |
| `o[]` | array<string> | no |  |
| `o[]ffset` | number | no |  |
| `o[]rdering` | string | no |  |
| `reason` | string | no |  |
| `updated_range_after` | date | no |  |
| `updated_range_before` | date | no |  |
| `warehouse` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "number": "string",
          "adjustmentType": "string",
          "actionPerformed": "string",
          "isComplete": true,
          "isTaskInProgress": true,
          "created": "2026-05-07T12:00:00.000Z",
          "updated": "2026-05-07T12:00:00.000Z",
          "totalQuantity": 1,
          "notes": "string",
          "id": 1,
          "warehouseId": 1,
          "reason": "string"
        }
      ],
      "count": 1,
      "next": "string",
      "previous": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].number` | string |  |
| `results[].adjustmentType` | string |  |
| `results[].actionPerformed` | string |  |
| `results[].isComplete` | boolean |  |
| `results[].isTaskInProgress` | boolean |  |
| `results[].created` | date |  |
| `results[].updated` | date |  |
| `results[].totalQuantity` | number |  |
| `results[].notes` | string |  |
| `results[].id` | number |  |
| `results[].warehouseId` | number |  |
| `results[].reason` | string |  |
| `count` | number |  |
| `next` | string |  |
| `previous` | object |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/stock/adjustment/documents/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stock-adjustment-documents.md) for the provider-specific parameters and requirements.

