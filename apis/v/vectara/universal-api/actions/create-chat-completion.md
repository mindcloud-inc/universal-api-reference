# Vectara: Create Chat Completion

Creates a chat completion in Vectara.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/create-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/create-chat-completion?connectionId=$CONNECTION_ID&model=string&messages%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "model": "string",
  "messages[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/create-chat-completion?${params}`, {
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
| `model` | string | yes | Model ID to use for the chat completion. |
| `messages[]` | array<object> | yes | Conversation messages array in OpenAI-compatible format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stream` | boolean | no | Whether to stream partial chat completion chunks. |
| `responseFormat` | object | no | Requested output format for the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {}
      ],
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<object> | Completion choices returned by the model. |
| `object` | string | The object type for the chat completion response. |

## Native endpoint

Through the native Vectara API, this operation is `POST /v2/llms/chat/completions` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-completion.md) for the provider-specific parameters and requirements.

