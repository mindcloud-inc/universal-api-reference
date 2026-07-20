# MailerLite: List Automations

Retrieves a page of automations from MailerLite.

```
GET https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-automations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-automations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-automations?${params}`, {
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
| `filter[enabled]` | boolean | no | Return active automations when true and inactive automations when false. |
| `filter[name]` | string | no | Filter automations by name. Example: `Welcome automation`. |
| `filter[group]` | string | no | Filter automations by trigger group ID. Example: `123456`. |
| `limit` | number | no | Number of automations to return per page. Example: `10`. |
| `page` | number | no | Page number to return. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "automationTemplateId": "string",
          "automationTemplateName": "Ava Chen",
          "broken": true,
          "complete": true,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "emailsCount": 1,
          "enabled": true,
          "firstEmailScreenshotUrl": "ava@example.com",
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
            {}
          ],
          "triggerData": {
            "brokenWorkflow": true,
            "completeWorkflow": true,
            "trackEcommerce": true
          },
          "triggers": [
            {}
          ],
          "warnings": [
            "string"
          ]
        }
      ],
      "links": {
        "first": "https://example.com",
        "last": "https://example.com",
        "next": "https://example.com",
        "prev": "https://example.com"
      },
      "meta": {
        "aggregations": {
          "all": 1,
          "drafts": 1,
          "unsync": 1,
          "workflows": 1
        },
        "currentPage": 1,
        "from": 1,
        "lastPage": 1,
        "links": [
          {
            "active": true,
            "label": "https://example.com",
            "url": "https://example.com"
          }
        ],
        "path": "string",
        "perPage": 1,
        "to": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].automationTemplateId` | string |  |
| `data[].automationTemplateName` | string |  |
| `data[].broken` | boolean |  |
| `data[].complete` | boolean |  |
| `data[].createdAt` | date |  |
| `data[].emailsCount` | number |  |
| `data[].enabled` | boolean |  |
| `data[].firstEmailScreenshotUrl` | string |  |
| `data[].hasBannedContent` | boolean |  |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].stats` | object |  |
| `data[].stats.bounceRate` | object |  |
| `data[].stats.bounceRate.float` | number |  |
| `data[].stats.bounceRate.string` | string |  |
| `data[].stats.clickRate` | object |  |
| `data[].stats.clickRate.float` | number |  |
| `data[].stats.clickRate.string` | string |  |
| `data[].stats.clicksCount` | number |  |
| `data[].stats.clickToOpenRate` | object |  |
| `data[].stats.clickToOpenRate.float` | number |  |
| `data[].stats.clickToOpenRate.string` | string |  |
| `data[].stats.completedSubscribersCount` | number |  |
| `data[].stats.forwardRate` | object |  |
| `data[].stats.forwardRate.float` | number |  |
| `data[].stats.forwardRate.string` | string |  |
| `data[].stats.hardBounceRate` | object |  |
| `data[].stats.hardBounceRate.float` | number |  |
| `data[].stats.hardBounceRate.string` | string |  |
| `data[].stats.hardBouncesCount` | number |  |
| `data[].stats.openRate` | object |  |
| `data[].stats.openRate.float` | number |  |
| `data[].stats.openRate.string` | string |  |
| `data[].stats.opensCount` | number |  |
| `data[].stats.sent` | number |  |
| `data[].stats.socialInteractionRate` | object |  |
| `data[].stats.socialInteractionRate.float` | number |  |
| `data[].stats.socialInteractionRate.string` | string |  |
| `data[].stats.socialInteractionsCount` | number |  |
| `data[].stats.softBounceRate` | object |  |
| `data[].stats.softBounceRate.float` | number |  |
| `data[].stats.softBounceRate.string` | string |  |
| `data[].stats.softBouncesCount` | number |  |
| `data[].stats.spamCount` | number |  |
| `data[].stats.spamRate` | object |  |
| `data[].stats.spamRate.float` | number |  |
| `data[].stats.spamRate.string` | string |  |
| `data[].stats.subscribersInQueueCount` | number |  |
| `data[].stats.uniqueClicksCount` | number |  |
| `data[].stats.uniqueOpensCount` | number |  |
| `data[].stats.unsubscribeRate` | object |  |
| `data[].stats.unsubscribeRate.float` | number |  |
| `data[].stats.unsubscribeRate.string` | string |  |
| `data[].stats.unsubscribesCount` | number |  |
| `data[].steps` | array<object> |  |
| `data[].triggerData` | object |  |
| `data[].triggerData.brokenWorkflow` | boolean |  |
| `data[].triggerData.completeWorkflow` | boolean |  |
| `data[].triggerData.trackEcommerce` | boolean |  |
| `data[].triggers` | array<object> |  |
| `data[].warnings` | array<string> |  |
| `links` | object |  |
| `links.first` | string |  |
| `links.last` | string |  |
| `links.next` | string |  |
| `links.prev` | string |  |
| `meta` | object |  |
| `meta.aggregations` | object |  |
| `meta.aggregations.all` | number |  |
| `meta.aggregations.drafts` | number |  |
| `meta.aggregations.unsync` | number |  |
| `meta.aggregations.workflows` | number |  |
| `meta.currentPage` | number |  |
| `meta.from` | number |  |
| `meta.lastPage` | number |  |
| `meta.links` | array<object> |  |
| `meta.links[].active` | boolean |  |
| `meta.links[].label` | string |  |
| `meta.links[].url` | string |  |
| `meta.path` | string |  |
| `meta.perPage` | number |  |
| `meta.to` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native MailerLite API, this operation is `GET /automations` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-automations.md) for the provider-specific parameters and requirements.

