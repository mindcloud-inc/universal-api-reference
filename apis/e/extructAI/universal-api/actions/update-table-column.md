# Extruct AI: Update Table Column

Updates a table column in Extruct AI.

```
PUT https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/update-table-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/update-table-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "string",
  "columnId": "string",
  "name": "Ava Chen",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/update-table-column', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "string",
    "columnId": "string",
    "name": "Ava Chen",
    "key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | Target table identifier. |
| `columnId` | string | yes | Target column identifier. |
| `name` | string | yes | Column display name. |
| `key` | string | yes | Column key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {
        "key": "string",
        "kind": "string",
        "name": "Ava Chen"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config.key` | string |  |
| `config.kind` | string |  |
| `config.name` | string |  |
| `created_at` | date |  |
| `id` | string |  |

## Native endpoint

Through the native Extruct AI API, this operation is `PATCH /v1/tables/:table_id/columns/:column_id` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-table-column.md) for the provider-specific parameters and requirements.

