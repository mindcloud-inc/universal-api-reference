# Sendloop: List Campaigns by Status



```
GET https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/list-campaigns-by-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/list-campaigns-by-status?connectionId=$CONNECTION_ID&campaignStatus=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignStatus": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/list-campaigns-by-status?${params}`, {
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
| `campaignStatus` | string | yes | Target campaign status: Draft, Scheduled, Outbox, or Sent |
| `limit` | number | no | Number of records to return |
| `page` | number | no | Page number to return Default: `1`. |
| `orderByField` | string | no | Sort field: CampaignID, CampaignName, or SendTime |
| `orderBySort` | string | no | Sort direction: ASC or DESC |
| `targetListId` | number | no | If provided, only campaigns sent to this list are returned |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignID": "string",
      "campaignMode": "string",
      "campaignName": "Ava Chen",
      "campaignStatus": "string",
      "currentStep": "string",
      "fetchURL": "https://example.com",
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "googleAnalyticsDomains": "string",
      "googleAnalyticsEnable": "string",
      "hTMLContent": "string",
      "newsletterTemplateType": "string",
      "plainContent": "string",
      "publicTinyContentLink": "https://example.com",
      "relNewsletterTemplateID": "string",
      "replyToEmail": "ava@example.com",
      "replyToName": "Ava Chen",
      "scheduleType": "string",
      "sendDate": "string",
      "sendProcessFinishedOn": "string",
      "sendProcessStartedOn": "string",
      "sendTime": "string",
      "sendTimeZone": "string",
      "subject": "string",
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
| `campaignMode` | string |  |
| `campaignName` | string |  |
| `campaignStatus` | string |  |
| `currentStep` | string |  |
| `fetchURL` | string |  |
| `fromEmail` | string |  |
| `fromName` | string |  |
| `googleAnalyticsDomains` | string |  |
| `googleAnalyticsEnable` | string |  |
| `hTMLContent` | string |  |
| `newsletterTemplateType` | string |  |
| `plainContent` | string |  |
| `publicTinyContentLink` | string |  |
| `relNewsletterTemplateID` | string |  |
| `replyToEmail` | string |  |
| `replyToName` | string |  |
| `scheduleType` | string |  |
| `sendDate` | string |  |
| `sendProcessFinishedOn` | string |  |
| `sendProcessStartedOn` | string |  |
| `sendTime` | string |  |
| `sendTimeZone` | string |  |
| `subject` | string |  |
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

Through the native Sendloop API, this operation is `POST /campaign.getlistbystatus/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns-by-status.md) for the provider-specific parameters and requirements.

