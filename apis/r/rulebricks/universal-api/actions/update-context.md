# Rulebricks: Update Context

Updates an existing context in Rulebricks.

```
PUT https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/update-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rulebricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/update-context" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/update-context', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `auto_execute_decisions` | boolean | no | Whether bound rules and flows auto-execute |
| `description` | string | no | Updated description of the context |
| `history_limit` | number | no | Maximum number of history entries to retain per field |
| `id` | string | yes | ID of the context to update |
| `name` | string | no | Updated name of the context |
| `on_schema_mismatch` | string | no | How to handle fields that do not match the schema |
| `schema` | object<object> | no | Context schema object. Runtime-proven shape requires a base array under schema.base |
| `slug` | string | no | Updated slug of the context |
| `ttl_seconds` | number | no | Time to live in seconds for live context instances |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Context ID |
| `name` | string | Context name |
| `slug` | string | Context slug |

## Native endpoint

Through the native Rulebricks API, this operation is `PUT /admin/contexts/:id` (base URL `https://rulebricks.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-context.md) for the provider-specific parameters and requirements.

