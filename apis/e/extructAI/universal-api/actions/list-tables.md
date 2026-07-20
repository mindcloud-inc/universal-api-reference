# Extruct AI: List Tables

Retrieves tables from Extruct AI.

```
GET https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/list-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/list-tables?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/list-tables?${params}`, {
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
| `kind` | string | no | Filter by table kind. One of: `0`, `1`, `2`. |
| `scope` | string | no | Filter by ownership scope. One of: `0`, `1`. |
| `search` | string | no | Case-insensitive search across table names and descriptions. |
| `tags[]` | array<string> | no | Repeat this parameter to match tables with any selected tag. |
| `sort` | string | no | Sort order for returned tables. One of: `0`, `1`, `2`, `3`, `4`, `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "num_rows": 1,
      "owner": {
        "email": "ava@example.com",
        "id": "string"
      },
      "scope": "string",
      "settings": {
        "exclude_from_search": true
      },
      "tags": [
        [
          "string"
        ]
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Table creation time. |
| `description` | string | Table description. |
| `id` | string | Table ID. |
| `kind` | string | Table kind. |
| `name` | string | Table name. |
| `num_rows` | number | Number of rows in the table. |
| `owner.email` | string | Owner email. |
| `owner.id` | string | Owner ID. |
| `scope` | string | Ownership scope. |
| `settings.exclude_from_search` | boolean | Whether the table is excluded from search. |
| `tags[]` | array<string> | Table tags. |
| `updated_at` | date | Last table update time. |

## Native endpoint

Through the native Extruct AI API, this operation is `GET /v1/tables` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tables.md) for the provider-specific parameters and requirements.

