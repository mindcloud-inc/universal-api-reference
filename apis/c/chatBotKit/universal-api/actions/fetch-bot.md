# ChatBotKit: Fetch Bot



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/fetch-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/fetch-bot?connectionId=$CONNECTION_ID&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/fetch-bot?${params}`, {
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
| `botId` | string | yes | The ID of the bot to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backstory": "string",
      "blueprintId": "string",
      "createdAt": 1,
      "datasetId": "string",
      "description": "string",
      "id": "string",
      "model": "string",
      "moderation": true,
      "name": "Ava Chen",
      "privacy": true,
      "skillsetId": "string",
      "updatedAt": 1,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backstory` | string |  |
| `blueprintId` | string |  |
| `createdAt` | number |  |
| `datasetId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `model` | string |  |
| `moderation` | boolean |  |
| `name` | string |  |
| `privacy` | boolean |  |
| `skillsetId` | string |  |
| `updatedAt` | number |  |
| `visibility` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `GET /bot/{botId}/fetch` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-bot.md) for the provider-specific parameters and requirements.

