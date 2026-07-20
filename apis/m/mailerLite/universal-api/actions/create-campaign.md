# MailerLite: Create Campaign

Creates a new campaign in MailerLite.

```
POST https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Disposable draft campaign",
  "type": "regular",
  "emails[]": [
    {}
  ],
  "emails[].subject": "Disposable test subject",
  "emails[].from_name": "MindCloud Test Sender",
  "emails[].from": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Disposable draft campaign",
    "type": "regular",
    "emails[]": [{}],
    "emails[].subject": "Disposable test subject",
    "emails[].from_name": "MindCloud Test Sender",
    "emails[].from": "apps@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Campaign name. Example: `Disposable draft campaign`. |
| `type` | string | yes | Campaign type. Example: `regular`. |
| `emails[]` | array<object> | yes | Email variants for the campaign. |
| `emails[].subject` | string | yes | Email subject line. Example: `Disposable test subject`. |
| `emails[].from_name` | string | yes | Verified sender name. Example: `MindCloud Test Sender`. |
| `emails[].from` | string | yes | Verified sender email address. Example: `apps@mindcloud.co`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_id` | number | no | Campaign language ID for unsubscribe content. Example: `4`. |
| `emails[].reply_to` | string | no | Verified reply-to email address. Example: `apps@mindcloud.co`. |
| `emails[].content` | string | no | Optional HTML content for advanced-plan custom HTML campaigns. Example: `<p>Hello from MindCloud</p>`. |
| `groups[]` | array<string> | no | Recipient group IDs. |
| `segments[]` | array<string> | no | Recipient segment IDs. Overrides groups when both are provided. |
| `settings` | object | no | Campaign settings object. |
| `settings.ecommerce_tracking` | boolean | no | Enable ecommerce link tracking for shop URLs. |

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
          "generateScreenshotTimestamp": "ava@example.com",
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
          "type": "ava@example.com",
          "updatedAt": "ava@example.com",
          "usesQuiz": true,
          "usesSurvey": true
        }
      ],
      "finishedAt": {},
      "hasBasicFilter": true,
      "hasWinner": {},
      "id": "string",
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
      "name": "Ava Chen",
      "needsRepair": true,
      "nextStep": {},
      "queuedAt": {},
      "recipientsCount": 1,
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
| `emails[].generateScreenshotTimestamp` | string |  |
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
| `emails[].type` | string |  |
| `emails[].updatedAt` | string |  |
| `emails[].usesQuiz` | boolean |  |
| `emails[].usesSurvey` | boolean |  |
| `finishedAt` | object |  |
| `hasBasicFilter` | boolean |  |
| `hasWinner` | object |  |
| `id` | string |  |
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
| `name` | string |  |
| `needsRepair` | boolean |  |
| `nextStep` | object |  |
| `queuedAt` | object |  |
| `recipientsCount` | number |  |
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

Through the native MailerLite API, this operation is `POST /campaigns` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

