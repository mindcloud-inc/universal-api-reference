# Baserow: Get Row

Retrieves a row from Baserow.

```
GET https://connect.mindcloud.co/v1/universal/baserow/latest/actions/get-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baserow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/get-row?connectionId=$CONNECTION_ID&tableId=1&rowId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "1",
  "rowId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baserow/latest/actions/get-row?${params}`, {
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
| `tableId` | number | yes | The Baserow table containing the row. |
| `rowId` | number | yes | The row to fetch. |
| `userFieldNames` | boolean | no | Use user-facing field names in the response. |
| `include` | string | no | Optional response metadata to include. |
| `view` | number | no | Optional view context for permissions and default values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "id": 1,
      "name": "Ava Chen",
      "order": "string",
      "started": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `order` | string |  |
| `started` | date |  |

## Native endpoint

Through the native Baserow API, this operation is `GET /api/database/rows/table/:table_id/:row_id/` (base URL `https://api.baserow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-row.md) for the provider-specific parameters and requirements.

