# SmartSuite: List Webhooks

Retrieves webhooks from SmartSuite.

```
GET https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&solutionId=69b45da87cb40fc74dbb4b83" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "solutionId": "69b45da87cb40fc74dbb4b83"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-webhooks?${params}`, {
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
| `solutionId` | string | yes | The SmartSuite solution ID to list webhooks for. Example: `69b45da87cb40fc74dbb4b83`. |
| `pageSize` | number | no | The number of webhook records to return per page. Default: `50`. Example: `50`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageToken` | string | no | The page token to continue listing webhooks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webhooks": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webhooks[].createdAt.at` | string |  |
| `webhooks[].createdAt.by` | string |  |
| `webhooks[].kinds[]` | string |  |
| `webhooks[].locator.accountId` | string |  |
| `webhooks[].locator.solutionId` | string |  |
| `webhooks[].notificationStatus.enabled.url` | string |  |
| `webhooks[].systemStatus.enabled.expiresAt` | string |  |
| `webhooks[].updatedAt.at` | string |  |
| `webhooks[].updatedAt.by` | string |  |
| `webhooks[].webhookId` | string |  |

## Native endpoint

Through the native SmartSuite API, this operation is `POST https://webhooks.smartsuite.com/smartsuite.webhooks.engine.Webhooks/ListWebhooks` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

