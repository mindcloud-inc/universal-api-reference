# xAI: Create Anthropic Message

Creates an Anthropic-style message in the xAI API.

```
POST https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-anthropic-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-anthropic-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-anthropic-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | no | Model name to use for the Anthropic-compatible message. |
| `max_tokens` | number | no | Maximum number of output tokens. |
| `messages[]` | array<object> | no | Input messages for the Anthropic-compatible request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {}
      ],
      "id": "string",
      "model": "string",
      "role": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | array<object> |  |
| `id` | string |  |
| `model` | string |  |
| `role` | string |  |
| `type` | string |  |

## Native endpoint

Through the native xAI API, this operation is `POST /messages` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-anthropic-message.md) for the provider-specific parameters and requirements.

