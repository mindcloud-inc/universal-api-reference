# MailerLite: List Campaigns

Retrieves campaigns from MailerLite by status or type.

```
GET https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-campaigns?${params}`, {
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
| `filter[status]` | string | no | Return campaigns by status: sent, draft, or ready. |
| `filter[type]` | string | no | Return campaigns by type: regular, ab, resend, or rss. |
| `limit` | number | no | Number of campaigns to return per page. Example: `25`. |
| `page` | number | no | Page number to return. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "basicFilterForHumans": {
        "allActiveSubscribers": true
      },
      "can": {
        "copy": true,
        "delete": true,
        "resend": true,
        "send": true,
        "update": true
      },
      "canBeCopied": true,
      "createdAt": "string",
      "defaultEmailId": "ava@example.com",
      "deliverySchedule": {},
      "ecommerceStats": {},
      "emails": [
        {
          "accountId": "ava@example.com",
          "createdAt": "ava@example.com",
          "emailableId": "ava@example.com",
          "emailableType": "ava@example.com",
          "from": "ava@example.com",
          "fromName": "ava@example.com",
          "generateScreenshotTimestamp": {},
          "id": "ava@example.com",
          "isDesigned": true,
          "isWinner": true,
          "language": {
            "direction": "ava@example.com",
            "id": "ava@example.com",
            "iso639": "ava@example.com",
            "name": "ava@example.com",
            "shortcode": "ava@example.com"
          },
          "languageId": 1,
          "name": {},
          "plainText": "ava@example.com",
          "preheader": {},
          "previewUrl": "ava@example.com",
          "replyTo": "ava@example.com",
          "screenshotUrl": {},
          "sendAfter": {},
          "stats": {
            "clickRate": {
              "float": 1,
              "string": "ava@example.com"
            },
            "clicksCount": 1,
            "clickToOpenRate": {
              "float": 1,
              "string": "ava@example.com"
            },
            "forwardRate": {
              "float": 1,
              "string": "ava@example.com"
            },
            "forwardsCount": 1,
            "hardBounceRate": {
              "float": 1,
              "string": "ava@example.com"
            },
            "hardBouncesCount": 1,
            "openRate": {
              "float": 1,
              "string": "ava@example.com"
            },
            "opensCount": 1,
            "sent": 1,
            "socialInteractionRate": {
              "float": 1,
              "string": "ava@example.com"
            },
            "socialInteractionsCount": 1,
            "softBounceRate": {
              "float": 1,
              "string": "ava@example.com"
            },
            "softBouncesCount": 1,
            "spamCount": 1,
            "spamRate": {
              "float": 1,
              "string": "ava@example.com"
            },
            "unsubscribeRate": {
              "float": 1,
              "string": "ava@example.com"
            },
            "unsubscribesCount": 1
          },
          "subject": "ava@example.com",
          "trackOpens": true,
          "type": {},
          "updatedAt": "ava@example.com",
          "usesQuiz": true,
          "usesSurvey": true
        }
      ],
      "finishedAt": {},
      "hasBasicFilter": true,
      "hasWinner": {},
      "id": "string",
      "initialCreatedAt": {},
      "isAppliedForSmartSendingIndexOption": true,
      "isCurrentlySendingOut": true,
      "isEligibleForSending": true,
      "isSmartSendingIndexOptionFinished": true,
      "isStopped": true,
      "language": {
        "direction": "string",
        "id": "string",
        "iso639": "string",
        "name": "Ava Chen",
        "shortcode": "string"
      },
      "languageId": "string",
      "missingData": [
        "string"
      ],
      "name": "Ava Chen",
      "needsRepair": true,
      "nextStep": {},
      "queuedAt": {},
      "scheduledFor": {},
      "settings": {
        "ecommerceTracking": true,
        "trackOpens": true,
        "useGoogleAnalytics": true
      },
      "startedAt": {},
      "status": "string",
      "stoppedAt": {},
      "type": "string",
      "typeForHumans": "string",
      "updatedAt": "string",
      "usedInAutomations": true,
      "usesEcommerce": true,
      "usesSurvey": true,
      "winnerSelectedManuallyAt": {},
      "winnerSendingTimeForHumans": {},
      "winnerVersionForHuman": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `basicFilterForHumans.allActiveSubscribers` | boolean |  |
| `can.copy` | boolean |  |
| `can.delete` | boolean |  |
| `can.resend` | boolean |  |
| `can.send` | boolean |  |
| `can.update` | boolean |  |
| `canBeCopied` | boolean |  |
| `createdAt` | string |  |
| `defaultEmailId` | string |  |
| `deliverySchedule` | object |  |
| `ecommerceStats` | object |  |
| `emails[].accountId` | string |  |
| `emails[].createdAt` | string |  |
| `emails[].emailableId` | string |  |
| `emails[].emailableType` | string |  |
| `emails[].from` | string |  |
| `emails[].fromName` | string |  |
| `emails[].generateScreenshotTimestamp` | object |  |
| `emails[].id` | string |  |
| `emails[].isDesigned` | boolean |  |
| `emails[].isWinner` | boolean |  |
| `emails[].language.direction` | string |  |
| `emails[].language.id` | string |  |
| `emails[].language.iso639` | string |  |
| `emails[].language.name` | string |  |
| `emails[].language.shortcode` | string |  |
| `emails[].languageId` | number |  |
| `emails[].name` | object |  |
| `emails[].plainText` | string |  |
| `emails[].preheader` | object |  |
| `emails[].previewUrl` | string |  |
| `emails[].replyTo` | string |  |
| `emails[].screenshotUrl` | object |  |
| `emails[].sendAfter` | object |  |
| `emails[].stats.clickRate.float` | number |  |
| `emails[].stats.clickRate.string` | string |  |
| `emails[].stats.clicksCount` | number |  |
| `emails[].stats.clickToOpenRate.float` | number |  |
| `emails[].stats.clickToOpenRate.string` | string |  |
| `emails[].stats.forwardRate.float` | number |  |
| `emails[].stats.forwardRate.string` | string |  |
| `emails[].stats.forwardsCount` | number |  |
| `emails[].stats.hardBounceRate.float` | number |  |
| `emails[].stats.hardBounceRate.string` | string |  |
| `emails[].stats.hardBouncesCount` | number |  |
| `emails[].stats.openRate.float` | number |  |
| `emails[].stats.openRate.string` | string |  |
| `emails[].stats.opensCount` | number |  |
| `emails[].stats.sent` | number |  |
| `emails[].stats.socialInteractionRate.float` | number |  |
| `emails[].stats.socialInteractionRate.string` | string |  |
| `emails[].stats.socialInteractionsCount` | number |  |
| `emails[].stats.softBounceRate.float` | number |  |
| `emails[].stats.softBounceRate.string` | string |  |
| `emails[].stats.softBouncesCount` | number |  |
| `emails[].stats.spamCount` | number |  |
| `emails[].stats.spamRate.float` | number |  |
| `emails[].stats.spamRate.string` | string |  |
| `emails[].stats.unsubscribeRate.float` | number |  |
| `emails[].stats.unsubscribeRate.string` | string |  |
| `emails[].stats.unsubscribesCount` | number |  |
| `emails[].subject` | string |  |
| `emails[].trackOpens` | boolean |  |
| `emails[].type` | object |  |
| `emails[].updatedAt` | string |  |
| `emails[].usesQuiz` | boolean |  |
| `emails[].usesSurvey` | boolean |  |
| `finishedAt` | object |  |
| `hasBasicFilter` | boolean |  |
| `hasWinner` | object |  |
| `id` | string |  |
| `initialCreatedAt` | object |  |
| `isAppliedForSmartSendingIndexOption` | boolean |  |
| `isCurrentlySendingOut` | boolean |  |
| `isEligibleForSending` | boolean |  |
| `isSmartSendingIndexOptionFinished` | boolean |  |
| `isStopped` | boolean |  |
| `language.direction` | string |  |
| `language.id` | string |  |
| `language.iso639` | string |  |
| `language.name` | string |  |
| `language.shortcode` | string |  |
| `languageId` | string |  |
| `missingData[]` | string |  |
| `name` | string |  |
| `needsRepair` | boolean |  |
| `nextStep` | object |  |
| `queuedAt` | object |  |
| `scheduledFor` | object |  |
| `settings.ecommerceTracking` | boolean |  |
| `settings.trackOpens` | boolean |  |
| `settings.useGoogleAnalytics` | boolean |  |
| `startedAt` | object |  |
| `status` | string |  |
| `stoppedAt` | object |  |
| `type` | string |  |
| `typeForHumans` | string |  |
| `updatedAt` | string |  |
| `usedInAutomations` | boolean |  |
| `usesEcommerce` | boolean |  |
| `usesSurvey` | boolean |  |
| `winnerSelectedManuallyAt` | object |  |
| `winnerSendingTimeForHumans` | object |  |
| `winnerVersionForHuman` | object |  |

## Native endpoint

Through the native MailerLite API, this operation is `GET /campaigns` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

