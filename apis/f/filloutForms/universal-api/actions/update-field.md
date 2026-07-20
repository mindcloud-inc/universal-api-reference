# Fillout Forms: Update Field

Updates an existing field in Fillout.

```
PUT https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/update-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/update-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "67ef4d500c50cce9",
  "tableId": "t7nUTgYUjzF",
  "fieldId": "vkuDPV6ZqBb"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/update-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "67ef4d500c50cce9",
    "tableId": "t7nUTgYUjzF",
    "fieldId": "vkuDPV6ZqBb"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | The unique identifier of the database Example: `67ef4d500c50cce9`. |
| `tableId` | string | yes | The unique identifier of the table. You can also use the table name instead of the ID. Example: `t7nUTgYUjzF`. |
| `fieldId` | string | yes | The unique identifier of the field. You can also use the field name instead of the ID. Example: `vkuDPV6ZqBb`. |
| `name` | string | no | New field name Example: `Customer Status`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template` | object | no | Updated field configuration. See the Fillout field types reference for the template shape for each field type. |

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
| `id` | string | Field identifier. |
| `name` | string | Field name. |
| `order` | number | Field display order. |
| `template` | object | Field template configuration. |
| `type` | string | Field type. |

## Native endpoint

Through the native Fillout Forms API, this operation is `PATCH https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields/:fieldId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-field.md) for the provider-specific parameters and requirements.

