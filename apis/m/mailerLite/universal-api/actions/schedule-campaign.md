# MailerLite: Schedule Campaign

Schedules a campaign in MailerLite, or sends it immediately.

```
PUT https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/schedule-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/schedule-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "123456789",
  "delivery": "scheduled",
  "schedule.date": "2026-03-06",
  "schedule.hours": "09",
  "schedule.minutes": "30"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/schedule-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "123456789",
    "delivery": "scheduled",
    "schedule.date": "2026-03-06",
    "schedule.hours": "09",
    "schedule.minutes": "30"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | Draft or ready campaign ID to schedule. Example: `123456789`. |
| `delivery` | string | yes | Delivery mode for the campaign. Example: `scheduled`. |
| `schedule` | object | no | Schedule settings object. |
| `schedule.date` | date | yes | Future delivery date. Example: `2026-03-06`. |
| `schedule.hours` | string | yes | Delivery hour in HH format. Example: `09`. |
| `schedule.minutes` | string | yes | Delivery minute in ii format. Example: `30`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schedule.timezone_id` | number | no | Timezone ID for scheduled delivery. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
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
      "deliverySchedule": "string",
      "emails": [
        [
          {}
        ]
      ],
      "finishedAt": "string",
      "hasBasicFilter": true,
      "id": "string",
      "isCurrentlySendingOut": true,
      "isEligibleForSending": true,
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
      "queuedAt": "string",
      "recipientsCount": 1,
      "scheduledFor": "string",
      "settings": {
        "ecommerceTracking": true,
        "trackOpens": true,
        "useGoogleAnalytics": true
      },
      "startedAt": "string",
      "status": "string",
      "stoppedAt": "string",
      "type": "string",
      "typeForHumans": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `can` | object |  |
| `can.copy` | boolean |  |
| `can.delete` | boolean |  |
| `can.resend` | boolean |  |
| `can.send` | boolean |  |
| `can.update` | boolean |  |
| `canBeCopied` | boolean |  |
| `createdAt` | string |  |
| `defaultEmailId` | string |  |
| `deliverySchedule` | string |  |
| `emails[]` | array<object> |  |
| `emails[].from` | string |  |
| `emails[].fromName` | string |  |
| `emails[].id` | string |  |
| `emails[].isDesigned` | boolean |  |
| `emails[].plainText` | string |  |
| `emails[].previewUrl` | string |  |
| `emails[].replyTo` | string |  |
| `emails[].subject` | string |  |
| `emails[].trackOpens` | boolean |  |
| `emails[].type` | string |  |
| `finishedAt` | string |  |
| `hasBasicFilter` | boolean |  |
| `id` | string |  |
| `isCurrentlySendingOut` | boolean |  |
| `isEligibleForSending` | boolean |  |
| `isStopped` | boolean |  |
| `language` | object |  |
| `language.direction` | string |  |
| `language.id` | string |  |
| `language.iso639` | string |  |
| `language.name` | string |  |
| `language.shortcode` | string |  |
| `languageId` | string |  |
| `missingData` | array<string> |  |
| `name` | string |  |
| `needsRepair` | boolean |  |
| `queuedAt` | string |  |
| `recipientsCount` | number |  |
| `scheduledFor` | string |  |
| `settings` | object |  |
| `settings.ecommerceTracking` | boolean |  |
| `settings.trackOpens` | boolean |  |
| `settings.useGoogleAnalytics` | boolean |  |
| `startedAt` | string |  |
| `status` | string |  |
| `stoppedAt` | string |  |
| `type` | string |  |
| `typeForHumans` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native MailerLite API, this operation is `POST /campaigns/:campaignId/schedule` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-campaign.md) for the provider-specific parameters and requirements.

