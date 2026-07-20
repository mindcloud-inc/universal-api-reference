# Wikibot: Ask Question With Query Parameters

Retrieves a bot answer from Wikibot with query parameters.

```
GET https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/ask-question-with-query-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wikibot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/ask-question-with-query-parameters?connectionId=$CONNECTION_ID&chatId=customer-123&query=How%20do%20I%20update%20my%20billing%20details%3F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "customer-123",
  "query": "How do I update my billing details?"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/ask-question-with-query-parameters?${params}`, {
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
| `chatId` | string | yes | External identifier for the customer chat. Example: `customer-123`. |
| `query` | string | yes | Question or message to send to Wikibot. Example: `How do I update my billing details?`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | list | no | Answer formatting mode. One of: `0`, `1`. Example: `links`. |
| `msgId` | string | no | Message identifier. Example: `msg-67890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": 1,
      "answer": "string",
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
| `botId` | string | Bot identifier. |
| `chatId` | string | External customer chat identifier. |
| `msgId` | string | Message identifier. |
| `type` | string | Response type, for example SUCCESS. |

## Native endpoint

Through the native Wikibot API, this operation is `GET /bot/ask` (base URL `https://api.wikibot.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ask-question-with-query-parameters.md) for the provider-specific parameters and requirements.

