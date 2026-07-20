# Graphor: Continue Document Conversation

Retrieves follow-up answers from Graphor with conversation memory.

```
GET https://connect.mindcloud.co/v1/universal/graphor/latest/actions/continue-document-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Graphor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/continue-document-conversation?connectionId=$CONNECTION_ID&conversationId=string&question=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string",
  "question": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphor/latest/actions/continue-document-conversation?${params}`, {
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
| `conversationId` | string | yes | Conversation identifier returned by a previous chat response. |
| `question` | string | yes | The follow-up question to ask. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "conversationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string |  |
| `conversationId` | string |  |

## Native endpoint

Through the native Graphor API, this operation is `POST /ask-sources` (base URL `https://sources.graphorlm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/continue-document-conversation.md) for the provider-specific parameters and requirements.

