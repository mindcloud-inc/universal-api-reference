# Extruct AI: Clone Table

Clones a table in Extruct AI.

```
POST https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/clone-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/clone-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/clone-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | Source table identifier. |
| `schemaOnly` | boolean | no | Defaults to false; set true to clone structure without data. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "child_relationships": [
        {}
      ],
      "columns": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "owner": {
        "email": "ava@example.com",
        "id": "string"
      },
      "parent_relationships": [
        {}
      ],
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `child_relationships` | array<object> |  |
| `columns` | array<object> |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `owner.email` | string |  |
| `owner.id` | string |  |
| `parent_relationships` | array<object> |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Extruct AI API, this operation is `POST /v1/tables/:table_id/clone` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clone-table.md) for the provider-specific parameters and requirements.

