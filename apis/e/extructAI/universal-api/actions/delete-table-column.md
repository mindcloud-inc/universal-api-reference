# Extruct AI: Delete Table Column

Deletes a table column from Extruct AI.

```
DELETE https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/delete-table-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/delete-table-column?connectionId=$CONNECTION_ID&tableId=string&columnId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "string",
  "columnId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/delete-table-column?${params}`, {
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
| `tableId` | string | yes | Target table identifier. |
| `columnId` | string | yes | Target column identifier. |

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

Through the native Extruct AI API, this operation is `DELETE /v1/tables/:table_id/columns/:column_id` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-table-column.md) for the provider-specific parameters and requirements.

