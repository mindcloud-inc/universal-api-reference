# DocsBot AI: Trigger Escalated Conversation Webhook Test

Triggers an escalated conversation webhook test in DocsBot AI.

```
POST https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/trigger-escalated-conversation-webhook-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/trigger-escalated-conversation-webhook-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/trigger-escalated-conversation-webhook-test', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": "string",
      "conversation": {},
      "event": "string",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | string |  |
| `conversation` | object |  |
| `event` | string |  |
| `teamId` | string |  |

## Native endpoint

Through the native DocsBot AI API, this operation is `POST /teams/:teamId/bots/:botId/webhooks/deliver-escalated` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-escalated-conversation-webhook-test.md) for the provider-specific parameters and requirements.

