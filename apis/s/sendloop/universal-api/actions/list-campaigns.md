# Sendloop: List Campaigns



```
GET https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/list-campaigns?${params}`, {
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
| `ignoreDrafts` | number | no | Set to 1 to exclude draft campaigns Default: `0`. |
| `ignoreSending` | number | no | Set to 1 to exclude currently sending campaigns Default: `0`. |
| `ignorePaused` | number | no | Set to 1 to exclude paused campaigns Default: `0`. |
| `ignoreSent` | number | no | Set to 1 to exclude sent campaigns Default: `0`. |
| `ignoreFailed` | number | no | Set to 1 to exclude failed campaigns Default: `0`. |
| `ignoreApproval` | number | no | Set to 1 to exclude approval-pending campaigns Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignID": "string",
      "campaignName": "Ava Chen",
      "campaignStatus": "string",
      "fetchURL": "https://example.com",
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "googleAnalyticsDomains": "string",
      "googleAnalyticsEnable": "string",
      "hTMLContent": "string",
      "lists": [
        "string"
      ],
      "plainContent": "string",
      "publicTinyContentLink": "https://example.com",
      "replyToEmail": "ava@example.com",
      "replyToName": "Ava Chen",
      "scheduleType": "string",
      "sendDate": "string",
      "sendProcessFinishedOn": "string",
      "sendTime": "string",
      "sendTimeZone": "string",
      "subject": "string",
      "thumbnailURL": true,
      "totalClicks": "string",
      "totalFailed": "string",
      "totalForwards": "string",
      "totalHardBounces": "string",
      "totalOpens": "string",
      "totalRecipients": "string",
      "totalSent": "string",
      "totalSoftBounces": "string",
      "totalUnsubscriptions": "string",
      "totalViewsOnBrowser": "string",
      "uniqueClicks": "string",
      "uniqueForwards": "string",
      "uniqueOpens": "string",
      "uniqueViewsOnBrowser": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignID` | string |  |
| `campaignName` | string |  |
| `campaignStatus` | string |  |
| `fetchURL` | string |  |
| `fromEmail` | string |  |
| `fromName` | string |  |
| `googleAnalyticsDomains` | string |  |
| `googleAnalyticsEnable` | string |  |
| `hTMLContent` | string |  |
| `lists[]` | string |  |
| `plainContent` | string |  |
| `publicTinyContentLink` | string |  |
| `replyToEmail` | string |  |
| `replyToName` | string |  |
| `scheduleType` | string |  |
| `sendDate` | string |  |
| `sendProcessFinishedOn` | string |  |
| `sendTime` | string |  |
| `sendTimeZone` | string |  |
| `subject` | string |  |
| `thumbnailURL` | boolean |  |
| `totalClicks` | string |  |
| `totalFailed` | string |  |
| `totalForwards` | string |  |
| `totalHardBounces` | string |  |
| `totalOpens` | string |  |
| `totalRecipients` | string |  |
| `totalSent` | string |  |
| `totalSoftBounces` | string |  |
| `totalUnsubscriptions` | string |  |
| `totalViewsOnBrowser` | string |  |
| `uniqueClicks` | string |  |
| `uniqueForwards` | string |  |
| `uniqueOpens` | string |  |
| `uniqueViewsOnBrowser` | string |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /campaign.getlist/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

