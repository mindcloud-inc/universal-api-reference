# SmartSuite: Create Webhook

Creates a new webhook in SmartSuite.

```
POST https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhook": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhook": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhook` | object | yes | The SmartSuite webhook object to create, including locator, kinds, filter, and notification_status. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webhook": {
        "createdAt": {
          "at": "string",
          "by": "string"
        },
        "kinds": [
          "string"
        ],
        "locator": {
          "accountId": "string",
          "solutionId": "string"
        },
        "notificationStatus": {
          "enabled": {
            "url": "https://example.com"
          }
        },
        "systemStatus": {
          "enabled": {
            "expiresAt": "string"
          }
        },
        "updatedAt": {
          "at": "string",
          "by": "string"
        },
        "webhookId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webhook.createdAt.at` | string |  |
| `webhook.createdAt.by` | string |  |
| `webhook.kinds[]` | string |  |
| `webhook.locator.accountId` | string |  |
| `webhook.locator.solutionId` | string |  |
| `webhook.notificationStatus.enabled.url` | string |  |
| `webhook.systemStatus.enabled.expiresAt` | string |  |
| `webhook.updatedAt.at` | string |  |
| `webhook.updatedAt.by` | string |  |
| `webhook.webhookId` | string |  |

## Native endpoint

Through the native SmartSuite API, this operation is `POST https://webhooks.smartsuite.com/smartsuite.webhooks.engine.Webhooks/CreateWebhook` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

