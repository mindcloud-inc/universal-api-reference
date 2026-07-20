# NocoDB: Create Field

Creates a new field in a NocoDB table.

```
POST https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/create-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "tableId": "string",
  "title": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "tableId": "string",
    "title": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseId` | string | yes | Base identifier. |
| `tableId` | string | yes | Table identifier. |
| `title` | string | yes | Title of the field. |
| `type` | string | yes | Field data type. |
| `description` | string | no | Description of the field. |
| `unique` | boolean | no | Whether the field should enforce unique values. |
| `options` | object | no | Field-type-specific options. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "default_value": "string",
      "description": "string",
      "id": "string",
      "options": {},
      "title": "string",
      "type": "string",
      "unique": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default_value` | string |  |
| `description` | string |  |
| `id` | string |  |
| `options` | object |  |
| `title` | string |  |
| `type` | string |  |
| `unique` | boolean |  |

## Native endpoint

Through the native NocoDB API, this operation is `POST /api/v3/meta/bases/:baseId/tables/:tableId/fields` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-field.md) for the provider-specific parameters and requirements.

