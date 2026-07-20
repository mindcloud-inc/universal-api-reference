# Dify: Update Conversation Variable

Updates an existing conversation variable in Dify.

```
PUT https://connect.mindcloud.co/v1/universal/dify/latest/actions/update-conversation-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dify/latest/actions/update-conversation-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "variableId": "string",
  "value": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dify/latest/actions/update-conversation-variable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "variableId": "string",
    "value": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | Conversation ID that owns the variable. |
| `variableId` | string | yes | Variable ID to update. |
| `value` | object | yes | New value for the variable. |
| `user` | string | no | User identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": 1,
      "value": {},
      "valueType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | number |  |
| `value` | object |  |
| `valueType` | string |  |

## Native endpoint

Through the native Dify API, this operation is `PUT /conversations/:conversation_id/variables/:variable_id` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation-variable.md) for the provider-specific parameters and requirements.

