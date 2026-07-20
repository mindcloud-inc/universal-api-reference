# xAI: Create Response

Creates a response in the xAI API.

```
POST https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-response', {
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
| `input` | string | no | Input text or structured input messages for the response. |
| `model` | string | no | Model name to use for the response. |
| `max_output_tokens` | number | no | Maximum output tokens for the response. |
| `store` | boolean | no | Whether xAI stores the response for later retrieval. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "model": "string",
      "object": "string",
      "output": [
        {}
      ],
      "status": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `model` | string |  |
| `object` | string |  |
| `output` | array<object> |  |
| `status` | string |  |
| `usage` | object |  |

## Native endpoint

Through the native xAI API, this operation is `POST /responses` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-response.md) for the provider-specific parameters and requirements.

