# Extruct AI: Create Table Columns

Creates table columns in Extruct AI.

```
POST https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/create-table-columns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/create-table-columns" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "string",
  "columnConfigs[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/create-table-columns', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "string",
    "columnConfigs[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | Target table identifier. |
| `columnConfigs[]` | array<object> | yes | List of new column config objects. |
| `insertAfter` | string | no | Defaults to true; may also be false or a column ID string. Default: `true`. |

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

Through the native Extruct AI API, this operation is `POST /v1/tables/:table_id/columns` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-table-columns.md) for the provider-specific parameters and requirements.

