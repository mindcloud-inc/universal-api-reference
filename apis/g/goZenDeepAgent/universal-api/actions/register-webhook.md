# GoZen DeepAgent: Register Webhook

Registers a webhook in GoZen DeepAgent.

```
POST https://connect.mindcloud.co/v1/universal/goZenDeepAgent/latest/actions/register-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoZen DeepAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goZenDeepAgent/latest/actions/register-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "knowledgebaseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goZenDeepAgent/latest/actions/register-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "knowledgebaseId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Webhook URL to receive lead collection events. |
| `knowledgebaseId` | string | yes | Chat bot ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "integrationId": "string",
      "knowledgebaseId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `integrationId` | string |  |
| `knowledgebaseId` | string |  |

## Native endpoint

Through the native GoZen DeepAgent API, this operation is `POST /integration/zapierapp/webhook` (base URL `https://api.deepbot.gozen.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-webhook.md) for the provider-specific parameters and requirements.

