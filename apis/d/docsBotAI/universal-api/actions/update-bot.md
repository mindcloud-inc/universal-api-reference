# DocsBot AI: Update Bot

Updates an existing bot in DocsBot AI.

```
PUT https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/update-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/update-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/update-bot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string",
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes | The DocsBot bot ID. |
| `teamId` | string | yes | The DocsBot team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chunkCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customPrompt": "string",
      "description": "string",
      "id": "string",
      "indexId": "string",
      "language": "string",
      "model": "string",
      "name": "Ava Chen",
      "pageCount": 1,
      "privacy": "string",
      "questionCount": 1,
      "sourceCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunkCount` | number |  |
| `createdAt` | date |  |
| `customPrompt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `indexId` | string |  |
| `language` | string |  |
| `model` | string |  |
| `name` | string |  |
| `pageCount` | number |  |
| `privacy` | string |  |
| `questionCount` | number |  |
| `sourceCount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native DocsBot AI API, this operation is `PUT /teams/:teamId/bots/:botId` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bot.md) for the provider-specific parameters and requirements.

