# Kadoa: Update Schema



```
PUT https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/update-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/update-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "schemaId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/update-schema', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "schemaId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entity` | string | no | Entity type |
| `fields` | list<object> | no | JSON array of field defs |
| `name` | string | no | Schema name |
| `schemaId` | string | yes | Schema ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "message": "string",
      "success": true,
      "updatedSchema": {
        "description": {},
        "entity": "string",
        "id": "string",
        "isPublic": true,
        "name": "Ava Chen",
        "schema": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | boolean |  |
| `message` | string |  |
| `success` | boolean |  |
| `updatedSchema.description` | object |  |
| `updatedSchema.entity` | string |  |
| `updatedSchema.id` | string |  |
| `updatedSchema.isPublic` | boolean |  |
| `updatedSchema.name` | string |  |
| `updatedSchema.schema` | array<object> |  |

## Native endpoint

Through the native Kadoa API, this operation is `PUT /v4/schemas/:schemaId` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-schema.md) for the provider-specific parameters and requirements.

