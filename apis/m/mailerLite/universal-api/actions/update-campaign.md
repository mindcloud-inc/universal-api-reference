# MailerLite: Update Campaign

Updates a draft campaign in MailerLite.

```
PUT https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "123456789",
  "name": "Updated disposable draft campaign",
  "emails[]": [
    {}
  ],
  "emails[].subject": "Updated disposable test subject",
  "emails[].from_name": "MindCloud Test Sender",
  "emails[].from": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "123456789",
    "name": "Updated disposable draft campaign",
    "emails[]": [{}],
    "emails[].subject": "Updated disposable test subject",
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
| `campaignId` | string | yes | Draft campaign ID to update. Example: `123456789`. |
| `name` | string | yes | Campaign name. Example: `Updated disposable draft campaign`. |
| `emails[]` | array<object> | yes | Email variants for the campaign. |
| `emails[].subject` | string | yes | Email subject line. Example: `Updated disposable test subject`. |
| `emails[].from_name` | string | yes | Verified sender name. Example: `MindCloud Test Sender`. |
| `emails[].from` | string | yes | Verified sender email address. Example: `apps@mindcloud.co`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_id` | number | no | Campaign language ID for unsubscribe content. Example: `4`. |
| `emails[].content` | string | no | Optional HTML content for advanced-plan custom HTML campaigns. Example: `<p>Updated from MindCloud</p>`. |
| `groups[]` | array<string> | no | Recipient group IDs. |
| `segments[]` | array<string> | no | Recipient segment IDs. Overrides groups when both are provided. |

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

Through the native MailerLite API, this operation is `PUT /campaigns/:campaignId` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

