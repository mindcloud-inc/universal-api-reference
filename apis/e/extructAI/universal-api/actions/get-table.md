# Extruct AI: Get Table

Retrieves a table from Extruct AI.

```
GET https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-table?connectionId=$CONNECTION_ID&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-table?${params}`, {
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

Through the native Extruct AI API, this operation is `GET /v1/tables/:table_id` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table.md) for the provider-specific parameters and requirements.

