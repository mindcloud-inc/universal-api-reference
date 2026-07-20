# Xano: Get Table

Retrieves a table from Xano by ID.

```
GET https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-table?connectionId=$CONNECTION_ID&table_id=1&workspace_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "table_id": "1",
  "workspace_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-table?${params}`, {
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
| `table_id` | number | yes |  |
| `workspace_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auth": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "docs": "string",
      "guid": "string",
      "id": 1,
      "index": [
        {
          "fields": [
            {
              "name": "Ava Chen"
            }
          ],
          "id": "string",
          "type": "string"
        }
      ],
      "name": "Ava Chen",
      "schema": [
        {
          "access": "string",
          "default": "string",
          "name": "Ava Chen",
          "nullable": true,
          "required": true,
          "style": "string",
          "type": "string"
        }
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `docs` | string |  |
| `guid` | string |  |
| `id` | number |  |
| `index[].fields[].name` | string |  |
| `index[].id` | string |  |
| `index[].type` | string |  |
| `name` | string |  |
| `schema[].access` | string |  |
| `schema[].default` | string |  |
| `schema[].name` | string |  |
| `schema[].nullable` | boolean |  |
| `schema[].required` | boolean |  |
| `schema[].style` | string |  |
| `schema[].type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Xano API, this operation is `GET /api%3Ameta/workspace/:workspace_id/table/:table_id` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table.md) for the provider-specific parameters and requirements.

