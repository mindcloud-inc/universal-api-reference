# Wikibot: Ask Question

Creates a bot answer in Wikibot.

```
POST https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/ask-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wikibot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/ask-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "customer-123",
  "query": "How do I update my billing details?"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/ask-question', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "customer-123",
    "query": "How do I update my billing details?"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | External identifier for the customer chat. Example: `customer-123`. |
| `query` | string | yes | Question or message to send to Wikibot. Example: `How do I update my billing details?`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | list | no | Answer formatting mode. One of: `0`, `1`. Example: `links`. |
| `msgId` | string | no | Message identifier. Example: `msg-67890`. |
| `attachments[]` | array<string> | no | Attachment URLs to include with the question. Accepts multiple values as an array. Example: `https://example.com/file.png`. |
| `agentId` | number | no | Identifier of the agent that should handle the request. Example: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": 1,
      "answer": "string",
      "attachments": [
        "string"
      ],
      "botId": "string",
      "chatId": "string",
      "msgId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | number | Agent identifier. |
| `answer` | string | Answer returned by Wikibot. |
| `attachments` | array<string> | Attachment URLs returned with the answer. |
| `botId` | string | Bot identifier. |
| `chatId` | string | External customer chat identifier. |
| `msgId` | string | Message identifier. |
| `type` | string | Response type, for example SUCCESS. |

## Native endpoint

Through the native Wikibot API, this operation is `POST /bot/ask` (base URL `https://api.wikibot.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ask-question.md) for the provider-specific parameters and requirements.

