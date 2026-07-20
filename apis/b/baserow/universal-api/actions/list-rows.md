# Baserow: List Rows

Retrieves rows from a Baserow table.

```
GET https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baserow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-rows?connectionId=$CONNECTION_ID&limit=25&offset=0&tableId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "tableId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-rows?${params}`, {
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
| `tableId` | number | yes | The Baserow table to read rows from. |
| `search` | string | no | Return only rows whose data matches this search query. |
| `searchMode` | string | no | Choose how Baserow should match the search term. |
| `include` | string | no | Comma-separated field names to include in the response. |
| `exclude` | string | no | Comma-separated field names to exclude from the response. |
| `userFieldNames` | boolean | no | Return field names instead of field IDs in the row payload. |
| `filters` | string | no | JSON serialized filter tree for advanced row filtering. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": {},
      "previous": {},
      "results": [
        {
          "active": true,
          "id": 1,
          "name": "Ava Chen",
          "order": "string",
          "started": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `next` | object |  |
| `previous` | object |  |
| `results[].active` | boolean |  |
| `results[].id` | number |  |
| `results[].name` | string |  |
| `results[].order` | string |  |
| `results[].started` | date |  |

## Native endpoint

Through the native Baserow API, this operation is `GET /api/database/rows/table/:table_id/` (base URL `https://api.baserow.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rows.md) for the provider-specific parameters and requirements.

