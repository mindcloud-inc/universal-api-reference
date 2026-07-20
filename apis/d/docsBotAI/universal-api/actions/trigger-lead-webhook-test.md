# DocsBot AI: Trigger Lead Webhook Test

Triggers a lead webhook delivery test in DocsBot AI.

```
POST https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/trigger-lead-webhook-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/trigger-lead-webhook-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/trigger-lead-webhook-test', {
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
      "event": "string",
      "lead": {},
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
| `event` | string |  |
| `lead` | object |  |
| `teamId` | string |  |

## Native endpoint

Through the native DocsBot AI API, this operation is `POST /teams/:teamId/bots/:botId/webhooks/deliver-lead` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-lead-webhook-test.md) for the provider-specific parameters and requirements.

