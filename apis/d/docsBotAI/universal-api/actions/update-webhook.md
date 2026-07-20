# DocsBot AI: Update Webhook

Updates an existing webhook in DocsBot AI.

```
PUT https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/update-webhook', {
  method: 'PUT',
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
      "events": [
        "string"
      ],
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string",
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<string> |  |
| `expirationDate` | date |  |
| `id` | string |  |
| `status` | string |  |
| `targetUrl` | string |  |

## Native endpoint

Through the native DocsBot AI API, this operation is `PATCH /teams/:teamId/bots/:botId/webhooks/:webhookId` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

