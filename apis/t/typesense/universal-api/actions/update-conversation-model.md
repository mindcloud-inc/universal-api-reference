# Typesense: Update Conversation Model

Updates a conversation model in Typesense.

```
PUT https://connect.mindcloud.co/v1/universal/typesense/latest/actions/update-conversation-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/update-conversation-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": {},
  "modelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typesense/latest/actions/update-conversation-model', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": {},
    "modelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | object | yes | Conversation model update JSON body. |
| `modelId` | string | yes | Conversation model ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "history_collection": "string",
      "id": "string",
      "model_name": "Ava Chen",
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `history_collection` | string |  |
| `id` | string |  |
| `model_name` | string |  |
| `response` | object |  |

## Native endpoint

Through the native Typesense API, this operation is `PUT /conversations/models/{{modelId}}` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation-model.md) for the provider-specific parameters and requirements.

