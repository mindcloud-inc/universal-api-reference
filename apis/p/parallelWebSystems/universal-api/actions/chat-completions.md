# Parallel Web Systems: Chat Completions



```
POST https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/chat-completions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/chat-completions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/chat-completions', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": {
        "delta": {
          "content": "string",
          "role": "string"
        },
        "finish_reason": "string"
      },
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices.delta.content` | string | Incremental response content. |
| `choices.delta.role` | string | Role for the streamed delta. |
| `choices.finish_reason` | string | Reason the completion finished. |
| `created` | date | Completion creation timestamp. |
| `id` | string | Chat completion identifier. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `POST /v1beta/chat/completions` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/chat-completions.md) for the provider-specific parameters and requirements.

