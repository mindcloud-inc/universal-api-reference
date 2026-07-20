# Reverse Contact: Fetch Person Comments



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-person-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-person-comments?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-person-comments?${params}`, {
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
| `url` | string | yes | Public Social profile URL whose comments should be fetched. |
| `webhookUrl` | string | no | HTTPS callback URL for live results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "status": "string",
        "webhookId": "string"
      },
      "metadata": {
        "executionTimeMs": 1,
        "requestId": "string"
      },
      "quotas": {
        "creditsConsumed": 1,
        "key": {
          "id": "string",
          "minuteRateLimit": {
            "left": 1,
            "limit": 1,
            "nextReset": "2026-05-07T12:00:00.000Z",
            "used": 1
          }
        },
        "workspace": {
          "allowDailyOvercost": true,
          "credits": {
            "left": 1,
            "total": 1,
            "used": 1
          },
          "hasUnlimitedCredits": true,
          "id": "string",
          "minuteRateLimit": {
            "left": 1,
            "limit": 1,
            "nextReset": "2026-05-07T12:00:00.000Z",
            "used": 1
          }
        }
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.status` | string |  |
| `data.webhookId` | string |  |
| `metadata.executionTimeMs` | number |  |
| `metadata.requestId` | string |  |
| `quotas.creditsConsumed` | number |  |
| `quotas.key.id` | string |  |
| `quotas.key.minuteRateLimit.left` | number |  |
| `quotas.key.minuteRateLimit.limit` | number |  |
| `quotas.key.minuteRateLimit.nextReset` | date |  |
| `quotas.key.minuteRateLimit.used` | number |  |
| `quotas.workspace.allowDailyOvercost` | boolean |  |
| `quotas.workspace.credits.left` | number |  |
| `quotas.workspace.credits.total` | number |  |
| `quotas.workspace.credits.used` | number |  |
| `quotas.workspace.hasUnlimitedCredits` | boolean |  |
| `quotas.workspace.id` | string |  |
| `quotas.workspace.minuteRateLimit.left` | number |  |
| `quotas.workspace.minuteRateLimit.limit` | number |  |
| `quotas.workspace.minuteRateLimit.nextReset` | date |  |
| `quotas.workspace.minuteRateLimit.used` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `POST /v2/fetch/persons/comments/live` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-person-comments.md) for the provider-specific parameters and requirements.

