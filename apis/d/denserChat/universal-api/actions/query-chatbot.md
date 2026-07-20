# DenserChat: Query Chatbot

Retrieves a chatbot answer from DenserChat.

```
GET https://connect.mindcloud.co/v1/universal/denserChat/latest/actions/query-chatbot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DenserChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/denserChat/latest/actions/query-chatbot?connectionId=$CONNECTION_ID&question=What%20are%20the%20pricing%20options%20for%20denserbot%3F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "question": "What are the pricing options for denserbot?"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/denserChat/latest/actions/query-chatbot?${params}`, {
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
| `question` | string | yes | The question to send to the Denser chatbot. Example: `What are the pricing options for denserbot?`. |
| `context[]` | array<object> | no | Prior conversation turns to send with the question. Example: `[object Object],[object Object]`. |
| `prompt` | string | no | An optional prompt override for this request. Example: `Please provide your answer in the following format: ...`. |
| `model` | list<string> | no | An optional model name for this request. One of: `claude-3-5-haiku`, `claude-3-5-sonnet`, `claude-3-7-sonnet`, `gpt-3.5`, `gpt-4`, `gpt-4o`, `gpt-4o-mini`. |
| `citation` | boolean | no | Whether to include citations in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "passages": [
        {}
      ],
      "statusCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string | The chatbot answer text. |
| `passages` | array<object> | The supporting citation passages returned by Denser. |
| `statusCode` | string | The status code reported in the Denser response body. |

## Native endpoint

Through the native DenserChat API, this operation is `POST /query` (base URL `https://denser.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-chatbot.md) for the provider-specific parameters and requirements.

