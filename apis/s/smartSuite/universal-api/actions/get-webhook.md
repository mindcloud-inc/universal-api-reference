# SmartSuite: Get Webhook

Retrieves a webhook from SmartSuite.

```
GET https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=69aceb11-1591-4568-9d81-41b8e44ec345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "69aceb11-1591-4568-9d81-41b8e44ec345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | yes | The SmartSuite webhook ID to fetch. Example: `69aceb11-1591-4568-9d81-41b8e44ec345`. |

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

Through the native SmartSuite API, this operation is `POST https://webhooks.smartsuite.com/smartsuite.webhooks.engine.Webhooks/GetWebhook` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

