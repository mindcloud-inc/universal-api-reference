# ChatBotKit: Update Bot



```
PUT https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/update-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/update-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/update-bot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes | The ID of the bot to update |
| `alias` | string | no | Alias for the bot |
| `name` | string | no | Name of the bot |
| `description` | string | no | Description of the bot |
| `meta` | object | no | Metadata for the bot |
| `model` | string | no | Model used by the bot |
| `backstory` | string | no | Backstory for the bot |
| `datasetId` | string | no | Dataset ID for the bot |
| `skillsetId` | string | no | Skillset ID for the bot |
| `privacy` | boolean | no | Whether the bot is private |
| `moderation` | boolean | no | Whether moderation is enabled |
| `blueprintId` | string | no | Blueprint ID for the bot |
| `visibility` | list | no | Visibility of the bot One of: `private`, `protected`, `public`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /bot/{botId}/update` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bot.md) for the provider-specific parameters and requirements.

