# NocoDB: Create Table

Creates a new table in NocoDB.

```
POST https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/create-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/create-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/create-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseId` | string | yes | Base identifier. |
| `title` | string | yes | Title of the table. |
| `description` | string | no | Description of the table. |
| `sourceId` | string | no | Data source identifier for sourced tables. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base_id": "string",
      "description": "string",
      "display_field_id": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "source_id": "string",
      "title": "string",
      "views": [
        {}
      ],
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_id` | string |  |
| `description` | string |  |
| `display_field_id` | string |  |
| `fields` | array<object> |  |
| `id` | string |  |
| `source_id` | string |  |
| `title` | string |  |
| `views` | array<object> |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native NocoDB API, this operation is `POST /api/v3/meta/bases/:baseId/tables` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-table.md) for the provider-specific parameters and requirements.

