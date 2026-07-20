# MailerLite: Get Automation

Retrieves a single automation from MailerLite.

```
GET https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-automation?connectionId=$CONNECTION_ID&automationId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "automationId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-automation?${params}`, {
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
| `automationId` | string | yes | MailerLite automation ID. Example: `123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automationTemplateId": "string",
      "automationTemplateName": "Ava Chen",
      "broken": true,
      "complete": true,
      "createdAt": "string",
      "emailsCount": 1,
      "enabled": true,
      "hasBannedContent": true,
      "id": "string",
      "name": "Ava Chen",
      "stats": {
        "bounceRate": {
          "float": 1,
          "string": "string"
        },
        "clickRate": {
          "float": 1,
          "string": "string"
        },
        "clicksCount": 1,
        "clickToOpenRate": {
          "float": 1,
          "string": "string"
        },
        "completedSubscribersCount": 1,
        "forwardRate": {
          "float": 1,
          "string": "string"
        },
        "hardBounceRate": {
          "float": 1,
          "string": "string"
        },
        "hardBouncesCount": 1,
        "openRate": {
          "float": 1,
          "string": "string"
        },
        "opensCount": 1,
        "sent": 1,
        "socialInteractionRate": {
          "float": 1,
          "string": "string"
        },
        "socialInteractionsCount": 1,
        "softBounceRate": {
          "float": 1,
          "string": "string"
        },
        "softBouncesCount": 1,
        "spamCount": 1,
        "spamRate": {
          "float": 1,
          "string": "string"
        },
        "subscribersInQueueCount": 1,
        "uniqueClicksCount": 1,
        "uniqueOpensCount": 1,
        "unsubscribeRate": {
          "float": 1,
          "string": "string"
        },
        "unsubscribesCount": 1
      },
      "steps": [
        [
          {}
        ]
      ],
      "triggerData": {
        "brokenWorkflow": true,
        "completeWorkflow": true,
        "trackEcommerce": true
      },
      "triggers": [
        [
          {}
        ]
      ],
      "warnings": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automationTemplateId` | string |  |
| `automationTemplateName` | string |  |
| `broken` | boolean |  |
| `complete` | boolean |  |
| `createdAt` | string |  |
| `emailsCount` | number |  |
| `enabled` | boolean |  |
| `hasBannedContent` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `stats` | object |  |
| `stats.bounceRate` | object |  |
| `stats.bounceRate.float` | number |  |
| `stats.bounceRate.string` | string |  |
| `stats.clickRate.float` | number |  |
| `stats.clickRate.string` | string |  |
| `stats.clicksCount` | number |  |
| `stats.clickToOpenRate` | object |  |
| `stats.clickToOpenRate.float` | number |  |
| `stats.clickToOpenRate.string` | string |  |
| `stats.completedSubscribersCount` | number |  |
| `stats.forwardRate.float` | number |  |
| `stats.forwardRate.string` | string |  |
| `stats.hardBounceRate.float` | number |  |
| `stats.hardBounceRate.string` | string |  |
| `stats.hardBouncesCount` | number |  |
| `stats.openRate.float` | number |  |
| `stats.openRate.string` | string |  |
| `stats.opensCount` | number |  |
| `stats.sent` | number |  |
| `stats.socialInteractionRate.float` | number |  |
| `stats.socialInteractionRate.string` | string |  |
| `stats.socialInteractionsCount` | number |  |
| `stats.softBounceRate.float` | number |  |
| `stats.softBounceRate.string` | string |  |
| `stats.softBouncesCount` | number |  |
| `stats.spamCount` | number |  |
| `stats.spamRate.float` | number |  |
| `stats.spamRate.string` | string |  |
| `stats.subscribersInQueueCount` | number |  |
| `stats.uniqueClicksCount` | number |  |
| `stats.uniqueOpensCount` | number |  |
| `stats.unsubscribeRate.float` | number |  |
| `stats.unsubscribeRate.string` | string |  |
| `stats.unsubscribesCount` | number |  |
| `steps[]` | array<object> |  |
| `triggerData` | object |  |
| `triggerData.brokenWorkflow` | boolean |  |
| `triggerData.completeWorkflow` | boolean |  |
| `triggerData.trackEcommerce` | boolean |  |
| `triggers[]` | array<object> |  |
| `warnings[]` | array<string> |  |

## Native endpoint

Through the native MailerLite API, this operation is `GET /automations/:automationId` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-automation.md) for the provider-specific parameters and requirements.

