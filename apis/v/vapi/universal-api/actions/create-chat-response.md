# Vapi: Create Chat Response

Creates an OpenAI-compatible chat response in Vapi.

```
POST https://connect.mindcloud.co/v1/universal/vapi/latest/actions/create-chat-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/create-chat-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vapi/latest/actions/create-chat-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assistantId` | string | no | This is the assistant that will be used for the chat. To use an existing assistant, use `assistantId` instead. |
| `assistant` | object | no |  |
| `assistantOverrides` | object | no |  |
| `squadId` | string | no | This is the squad that will be used for the chat. To use a transient squad, use `squad` instead. |
| `squad` | object | no |  |
| `name` | string | no | This is the name of the chat. This is just for your own reference. |
| `sessionId` | string | no | This is the ID of the session that will be used for the chat. Mutually exclusive with previousChatId. |
| `input` | string | yes |  |
| `previousChatId` | string | no | This is the ID of the chat that will be used as context for the new chat. The messages from the previous chat will be used as context. Mutually exclusive with sessionId. |
| `transport` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "error": "string",
      "id": "string",
      "object": "string",
      "output": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number | Unix timestamp (in seconds) of when this Response was created |
| `error` | string | Error message if the response failed |
| `id` | string | Unique identifier for this Response |
| `object` | string | The object type |
| `output` | array<object> | Output messages from the model |
| `status` | string | Status of the response |

## Native endpoint

Through the native Vapi API, this operation is `POST /chat/responses` (base URL `https://api.vapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-response.md) for the provider-specific parameters and requirements.

