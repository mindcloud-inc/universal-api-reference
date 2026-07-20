# Fillout: Update Field

Updates a field in Fillout.

```
PUT https://connect.mindcloud.co/v1/universal/fillout/latest/actions/update-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fillout/latest/actions/update-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "tableId": "string",
  "fieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fillout/latest/actions/update-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "tableId": "string",
    "fieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | The database identifier. |
| `tableId` | string | yes | The table identifier. |
| `fieldId` | string | yes | The field identifier. |
| `name` | string | no | The updated field name. |
| `template` | object | no | Optional field template configuration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "order": 1,
      "template": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `order` | number |  |
| `template` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Fillout API, this operation is `PATCH https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields/:fieldId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-field.md) for the provider-specific parameters and requirements.

