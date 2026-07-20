# GPT Chatbot: Delete Chatbot

Deletes an existing chatbot from GPT Chatbot.

```
DELETE https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/delete-chatbot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/delete-chatbot?connectionId=$CONNECTION_ID&chatbotUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatbotUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/delete-chatbot?${params}`, {
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
| `chatbotUuid` | string | yes | Chatbot uuid. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native GPT Chatbot API, this operation is `DELETE /chatbot/:uuid/delete` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-chatbot.md) for the provider-specific parameters and requirements.

