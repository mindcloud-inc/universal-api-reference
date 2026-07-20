# Watbot: Add List Schema Field

Adds a field to a list schema in Watbot.

```
PUT https://connect.mindcloud.co/v1/universal/watbot/latest/actions/add-list-schema-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/add-list-schema-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "field": "[object Object]",
  "schemaId": "5dee4800c2cc5a38ec797235"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/watbot/latest/actions/add-list-schema-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "field": "[object Object]",
    "schemaId": "5dee4800c2cc5a38ec797235"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `field` | object | yes | Field definition object. Example: `[object Object]`. |
| `schemaId` | string | yes | ID of the list schema. Example: `5dee4800c2cc5a38ec797235`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fields": {},
      "id": "string",
      "isMenu": true,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | List schema creation timestamp. |
| `fields` | object | Field definitions keyed by field slug. |
| `id` | string | List schema ID. |
| `isMenu` | boolean | Whether the list is shown in the Watbot menu. |
| `name` | string | List schema name. |
| `updatedAt` | date | List schema update timestamp. |

## Native endpoint

Through the native Watbot API, this operation is `POST /addListSchemaField` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-list-schema-field.md) for the provider-specific parameters and requirements.

