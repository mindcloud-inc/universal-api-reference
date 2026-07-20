# Chatling: Retrieve Chatbot

Retrieves a chatbot from Chatling.

```
GET https://connect.mindcloud.co/v1/universal/chatling/latest/actions/retrieve-chatbot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/retrieve-chatbot?connectionId=$CONNECTION_ID&chatbotId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatbotId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatling/latest/actions/retrieve-chatbot?${params}`, {
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
| `chatbotId` | string | yes | The chatbot ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "version": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `version` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Chatling API, this operation is `GET /chatbots/:chatbotId` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-chatbot.md) for the provider-specific parameters and requirements.

