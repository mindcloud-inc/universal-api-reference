# ChatBotKit: Fetch Conversation



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/fetch-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/fetch-conversation?connectionId=$CONNECTION_ID&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/fetch-conversation?${params}`, {
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
| `conversationId` | string | yes | The ID of the conversation to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backstory": "string",
      "botId": "string",
      "contactId": "string",
      "createdAt": 1,
      "datasetId": "string",
      "description": "string",
      "id": "string",
      "model": "string",
      "moderation": true,
      "name": "Ava Chen",
      "privacy": true,
      "skillsetId": "string",
      "taskId": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backstory` | string |  |
| `botId` | string |  |
| `contactId` | string |  |
| `createdAt` | number |  |
| `datasetId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `model` | string |  |
| `moderation` | boolean |  |
| `name` | string |  |
| `privacy` | boolean |  |
| `skillsetId` | string |  |
| `taskId` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `GET /conversation/{conversationId}/fetch` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-conversation.md) for the provider-specific parameters and requirements.

