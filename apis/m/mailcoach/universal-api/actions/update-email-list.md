# Mailcoach: Update Email List

Updates an existing email list in Mailcoach.

```
PUT https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/update-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailcoach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/update-email-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "defaultFromEmail": "ava@example.com",
  "name": "Ava Chen",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/update-email-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "defaultFromEmail": "ava@example.com",
    "name": "Ava Chen",
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowFormSubscriptions` | boolean | no | Whether form subscriptions are allowed. |
| `campaignsFeedEnabled` | boolean | no | Whether the campaigns feed is enabled for the list. |
| `confirmationMail` | string | no | The confirmation mail mode. |
| `confirmationMailContent` | string | no | The content used for a custom confirmation email. |
| `confirmationMailSubject` | string | no | The subject used for a custom confirmation email. |
| `defaultFromEmail` | string | yes | The default sender email address. |
| `defaultFromName` | string | no | The default sender name. |
| `defaultReplyToEmail` | string | no | The default reply-to email address. |
| `defaultReplyToName` | string | no | The default reply-to name. |
| `name` | string | yes | The name of the email list. |
| `redirectAfterAlreadySubscribed` | string | no | URL to redirect to when the subscriber already exists. |
| `redirectAfterSubscribed` | string | no | URL to redirect to after a successful subscription. |
| `redirectAfterSubscriptionPending` | string | no | URL to redirect to when confirmation is still pending. |
| `redirectAfterUnsubscribed` | string | no | URL to redirect to after an unsubscribe. |
| `reportCampaignSent` | boolean | no | Whether to send campaign sent reports. |
| `reportCampaignSummary` | boolean | no | Whether to send campaign summary reports. |
| `reportEmailListSummary` | boolean | no | Whether to send email list summary reports. |
| `reportRecipients` | string | no | Comma-delimited email addresses that should receive reports. |
| `requiresConfirmation` | boolean | no | Whether subscribers must confirm before they are added. |
| `uuid` | string | yes | The UUID of the email list to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowFormSubscriptions": true,
      "campaignsFeedEnabled": true,
      "confirmationMail": "string",
      "confirmationMailContent": "string",
      "confirmationMailSubject": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultFromEmail": "ava@example.com",
      "defaultFromName": "Ava Chen",
      "defaultReplyToEmail": "ava@example.com",
      "defaultReplyToName": "Ava Chen",
      "name": "Ava Chen",
      "redirectAfterAlreadySubscribed": "string",
      "redirectAfterSubscribed": "string",
      "redirectAfterSubscriptionPending": "string",
      "redirectAfterUnsubscribed": "string",
      "reportCampaignSent": true,
      "reportCampaignSummary": true,
      "reportEmailListSummary": true,
      "reportRecipients": "string",
      "requiresConfirmation": true,
      "segmentsCount": 1,
      "subscribersCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowFormSubscriptions` | boolean |  |
| `campaignsFeedEnabled` | boolean |  |
| `confirmationMail` | string |  |
| `confirmationMailContent` | string |  |
| `confirmationMailSubject` | string |  |
| `createdAt` | date |  |
| `defaultFromEmail` | string |  |
| `defaultFromName` | string |  |
| `defaultReplyToEmail` | string |  |
| `defaultReplyToName` | string |  |
| `name` | string |  |
| `redirectAfterAlreadySubscribed` | string |  |
| `redirectAfterSubscribed` | string |  |
| `redirectAfterSubscriptionPending` | string |  |
| `redirectAfterUnsubscribed` | string |  |
| `reportCampaignSent` | boolean |  |
| `reportCampaignSummary` | boolean |  |
| `reportEmailListSummary` | boolean |  |
| `reportRecipients` | string |  |
| `requiresConfirmation` | boolean |  |
| `segmentsCount` | number |  |
| `subscribersCount` | number |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mailcoach API, this operation is `PUT /email-lists/:uuid` (base URL `https://mindcloud.mailcoach.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-email-list.md) for the provider-specific parameters and requirements.

