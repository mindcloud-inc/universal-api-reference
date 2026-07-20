# SparrowDesk: Update Conversation Field

Updates an existing conversation field in SparrowDesk.

```
PUT https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/update-conversation-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/update-conversation-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/update-conversation-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Updated conversation field description. |
| `id` | number | yes | SparrowDesk conversation field ID. |
| `isActive` | boolean | no | Set true to keep the field active. |
| `name` | string | no | Updated conversation field name. |
| `type` | string | no | Updated conversation field type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "description": "string",
      "fieldOptions": [
        {}
      ],
      "id": 1,
      "internalName": "Ava Chen",
      "isActive": true,
      "isDefault": true,
      "isMandatoryOnClose": true,
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Creation timestamp. |
| `description` | string | Field description. |
| `fieldOptions` | array<object> | Selectable field options. |
| `id` | number | Conversation field ID. |
| `internalName` | string | Internal field key. |
| `isActive` | boolean | Whether the field is active. |
| `isDefault` | boolean | Whether the field is a default field. |
| `isMandatoryOnClose` | boolean | Whether the field is required when closing a conversation. |
| `name` | string | Field label. |
| `type` | string | Field type. |
| `updatedAt` | number | Last update timestamp. |

## Native endpoint

Through the native SparrowDesk API, this operation is `PATCH /conversations/fields/{{id}}` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation-field.md) for the provider-specific parameters and requirements.

