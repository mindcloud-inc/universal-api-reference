# ManyReach: List Campaigns

Retrieves campaigns from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-campaigns?${params}`, {
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
| `page` | number | no | Page number (1-indexed). Example: `1`. |
| `limit` | number | no | Items per page. Default 100, max 1000. Example: `100`. |
| `startingAfter` | number | no | Cursor for the next page. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeProspectCount": 1,
      "body": "string",
      "bounceCount": 1,
      "campaignId": 1,
      "clickCount": 1,
      "conversionCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dailyLimit": 1,
      "description": "string",
      "folderId": 1,
      "fromEmails": "ava@example.com",
      "fromName": "Ava Chen",
      "interestedCount": 1,
      "name": "Ava Chen",
      "openCount": 1,
      "prospectCount": 1,
      "replyCount": 1,
      "replyToEmail": "ava@example.com",
      "sentCount": 1,
      "status": "string",
      "subject": "string",
      "textOnlyEmails": true,
      "trackClicks": true,
      "trackOpens": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeProspectCount` | number | Total number of active prospects in the campaign. |
| `body` | string | HTML email body content for the initial campaign message. |
| `bounceCount` | number | Total number of bounces across the campaign. |
| `campaignId` | number | Unique identifier for the email campaign. |
| `clickCount` | number | Total number of link clicks across the campaign. |
| `conversionCount` | number | Total number of conversions tracked across the campaign. |
| `createdAt` | date | Timestamp when the campaign was created in the system. |
| `dailyLimit` | number | Maximum number of emails the campaign can send per day. |
| `description` | string | Optional campaign description. |
| `folderId` | number | Folder identifier for organizing and grouping campaigns. |
| `fromEmails` | string | Comma-separated sender email addresses. |
| `fromName` | string | Display name shown in the From field. |
| `interestedCount` | number | Total number of prospects marked as interested. |
| `name` | string | Campaign display name. |
| `openCount` | number | Total number of email opens across the campaign. |
| `prospectCount` | number | Total number of prospects enrolled in the campaign. |
| `replyCount` | number | Total number of replies across the campaign. |
| `replyToEmail` | string | Reply-to email address. |
| `sentCount` | number | Total number of emails sent across the campaign. |
| `status` | string | Current campaign status. |
| `subject` | string | Initial campaign email subject line. |
| `textOnlyEmails` | boolean | Whether emails are sent in plain text only. |
| `trackClicks` | boolean | Whether link clicks are tracked. |
| `trackOpens` | boolean | Whether email opens are tracked. |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/campaigns` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

