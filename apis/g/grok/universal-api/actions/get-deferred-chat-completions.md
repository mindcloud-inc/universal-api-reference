# Grok: Get Deferred Chat Completions

Retrieves deferred chat completion results from Grok.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-deferred-chat-completions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-deferred-chat-completions?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-deferred-chat-completions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | Deferred request identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {
          "finishReason": "string",
          "index": 1,
          "message": {
            "content": "string",
            "role": "string"
          }
        }
      ],
      "created": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "usage": {
        "completionTokens": 1,
        "promptTokens": 1,
        "totalTokens": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<object> | Completion choices returned by xAI. |
| `choices[].finishReason` | string | Reason the choice finished. |
| `choices[].index` | number | Choice index. |
| `choices[].message` | object | Assistant message for the choice. |
| `choices[].message.content` | string | Text content for the returned message. |
| `choices[].message.role` | string | Role for the returned message. |
| `created` | number | Unix timestamp when the completion was created. |
| `id` | string | Chat completion identifier. |
| `model` | string | Model used to generate the completion. |
| `object` | string | Provider object type. |
| `usage` | object | Token usage metadata for the completion. |
| `usage.completionTokens` | number | Completion token count. |
| `usage.promptTokens` | number | Prompt token count. |
| `usage.totalTokens` | number | Total token count. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/chat/deferred-completion/:request_id` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deferred-chat-completions.md) for the provider-specific parameters and requirements.

