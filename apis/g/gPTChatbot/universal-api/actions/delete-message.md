# GPT Chatbot: Delete Message

Deletes an existing message from GPT Chatbot.

```
DELETE https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/delete-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/delete-message?connectionId=$CONNECTION_ID&messageUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/delete-message?${params}`, {
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
| `messageUuid` | string | yes | Message uuid. |

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

Through the native GPT Chatbot API, this operation is `POST /message/:uuid/delete` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message.md) for the provider-specific parameters and requirements.

