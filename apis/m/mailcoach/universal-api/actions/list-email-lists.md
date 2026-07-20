# Mailcoach: List Email Lists

Retrieves all email lists from Mailcoach.

```
GET https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/list-email-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailcoach `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/list-email-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/list-email-lists?${params}`, {
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
| `filterName` | string | no | Filter email lists by exact name. |
| `filterSearch` | string | no | Search email lists by name. |

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

Through the native Mailcoach API, this operation is `GET /email-lists` (base URL `https://mindcloud.mailcoach.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-lists.md) for the provider-specific parameters and requirements.

