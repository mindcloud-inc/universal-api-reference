# ManyReach: Get Campaign

Retrieves a campaign from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-campaign?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-campaign?${params}`, {
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
| `id` | number | yes | Unique identifier of the campaign to retrieve. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeProspectCount": 1,
      "bccEmails": "ava@example.com",
      "body": "string",
      "bounceCount": 1,
      "campaignId": 1,
      "ccEmails": "ava@example.com",
      "clickCount": 1,
      "conversionCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dailyLimit": 1,
      "dailyLimitIncrease": true,
      "dailyLimitIncreasePercent": 1,
      "dailyLimitIncreaseToMax": 1,
      "dailyLimitInitial": 1,
      "dailyLimitInitialEnabled": true,
      "dailyLimitOnDate": "2026-05-07T12:00:00.000Z",
      "dailyLimitPer": "string",
      "dailyLimitPrioritize": "string",
      "dailyLimitWhichEmailsCount": "ava@example.com",
      "deactivateIfMissingPlaceholder": true,
      "delayMinMinutes": 1,
      "description": "string",
      "espLimitEnabled": true,
      "espLimitToGoogle": true,
      "espLimitToMicrosoft": true,
      "espLimitToOther": true,
      "espMatchEnabled": true,
      "espMatchType": "string",
      "folderId": 1,
      "fromEmails": "ava@example.com",
      "fromName": "Ava Chen",
      "initialBounceCount": 1,
      "initialClickCount": 1,
      "initialConversionCount": 1,
      "initialInterestedCount": 1,
      "initialOpenCount": 1,
      "initialReplyCount": 1,
      "interestedCount": 1,
      "name": "Ava Chen",
      "openCount": 1,
      "prospectCount": 1,
      "prospectValue": 1,
      "replyBccEmails": "ava@example.com",
      "replyCcEmails": "ava@example.com",
      "replyCount": 1,
      "replyToEmail": "ava@example.com",
      "scheduleSending": true,
      "scheduleSendOnDate": "2026-05-07T12:00:00.000Z",
      "scheduleSendOnDateEnabled": true,
      "scheduleSendOnDateHours": 1,
      "scheduleSendOnDateMinutes": 1,
      "scheduleTimeZone": "string",
      "sendFri": true,
      "sendFriAfter": 1,
      "sendFriBefore": 1,
      "sendMon": true,
      "sendMonAfter": 1,
      "sendMonBefore": 1,
      "sendSat": true,
      "sendSatAfter": 1,
      "sendSatBefore": 1,
      "sendSun": true,
      "sendSunAfter": 1,
      "sendSunBefore": 1,
      "sendThu": true,
      "sendThuAfter": 1,
      "sendThuBefore": 1,
      "sendTue": true,
      "sendTueAfter": 1,
      "sendTueBefore": 1,
      "sendUnsubscribeListHeader": true,
      "sendWed": true,
      "sendWedAfter": 1,
      "sendWedBefore": 1,
      "sentCount": 1,
      "status": "string",
      "stopCoworkersOnReply": true,
      "subject": "string",
      "textOnlyEmails": true,
      "trackClicks": true,
      "trackOpens": true,
      "useProspectsTimeZone": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeProspectCount` | number | Total number of prospects currently active and enrolled in this campaign. |
| `bccEmails` | string | Comma-separated list of email addresses to include as BCC (blind carbon copy) recipients on all campaign emails. |
| `body` | string | HTML email body content for the initial campaign message. |
| `bounceCount` | number | Total number of bounce responses received across all campaign emails. |
| `campaignId` | number | Unique identifier for the email campaign. |
| `ccEmails` | string | Comma-separated list of email addresses to include as CC (carbon copy) recipients on all campaign emails. |
| `clickCount` | number | Total number of link clicks within all campaign emails. |
| `conversionCount` | number | Total number of conversions tracked across all campaign emails. |
| `createdAt` | date | Timestamp when the campaign was created in the system. |
| `dailyLimit` | number | Maximum number of emails this campaign can send per day; must be between 1 and 10,000. |
| `dailyLimitIncrease` | boolean | Enable automatic progressive increase of the daily sending limit to gradually scale up capacity. |
| `dailyLimitIncreasePercent` | number | Daily percentage increase applied to the sending limit when progressive increase is enabled; must be between 0 and 10,000. |
| `dailyLimitIncreaseToMax` | number | Target maximum daily sending limit when progressive increase is enabled; must be between 0 and 10,000. |
| `dailyLimitInitial` | number | Separate daily sending limit specifically for initial campaign emails; must be between 1 and 10,000. |
| `dailyLimitInitialEnabled` | boolean | Enable separate daily limit for initial campaign emails distinct from overall campaign limit. |
| `dailyLimitOnDate` | date | Current calculated daily limit after applying progressive increases. |
| `dailyLimitPer` | string | Scope for applying the daily limit: 'sender' applies limit per sender account, 'campaign' applies limit across entire campaign. |
| `dailyLimitPrioritize` | string | Email prioritization strategy when approaching daily limit: 'initial' prioritizes first emails, 'followup' prioritizes follow-up emails. |
| `dailyLimitWhichEmailsCount` | string | Which email types count toward daily limit: 'all' counts everything, 'initial' counts only first emails, 'followup' counts only followups. |
| `deactivateIfMissingPlaceholder` | boolean | Automatically deactivate prospect from campaign if required email placeholder/merge tag is missing from their data. |
| `delayMinMinutes` | number | Minimum delay in minutes between sending consecutive emails to avoid spam filters; must be between 1 and 1,440 (24 hours). |
| `description` | string | Optional description explaining the purpose or goal of this campaign; maximum 512 characters. |
| `espLimitEnabled` | boolean | Enable ESP limiting to restrict campaign sends to specific email service providers. |
| `espLimitToGoogle` | boolean | Include Google email providers when ESP limiting is enabled. |
| `espLimitToMicrosoft` | boolean | Include Microsoft email providers when ESP limiting is enabled. |
| `espLimitToOther` | boolean | Include other email providers beyond Microsoft and Google when ESP limiting is enabled. |
| `espMatchEnabled` | boolean | Enable ESP matching to send emails from senders that match the prospect's email provider for better deliverability. |
| `espMatchType` | string | ESP (Email Service Provider) matching strategy type: none, match sender, or match domain. |
| `folderId` | number | Folder identifier for organizing and grouping campaigns; must be a positive integer. |
| `fromEmails` | string | Comma-separated list of sender email addresses to use for sending campaign emails. |
| `fromName` | string | Display name shown in the From field of campaign emails; maximum 128 characters. |
| `initialBounceCount` | number | Number of bounces from the initial campaign email only (excluding followups). |
| `initialClickCount` | number | Number of link clicks from the initial campaign email only (excluding followups). |
| `initialConversionCount` | number | Number of conversions from the initial campaign email only (excluding followups). |
| `initialInterestedCount` | number | Number of prospects marked as interested from the initial campaign email only (excluding followups). |
| `initialOpenCount` | number | Number of email opens from the initial campaign email only (excluding followups). |
| `initialReplyCount` | number | Number of replies from the initial campaign email only (excluding followups). |
| `interestedCount` | number | Total number of prospects marked as interested across all campaign emails. |
| `name` | string | Campaign display name for identification and organization; maximum 256 characters. |
| `openCount` | number | Total number of email opens across all campaign emails. |
| `prospectCount` | number | Total number of prospects enrolled in this campaign. |
| `prospectValue` | number | Estimated monetary value per prospect conversion for ROI tracking; must be a positive integer. |
| `replyBccEmails` | string | Comma-separated list of email addresses to BCC on prospect reply emails for internal tracking. |
| `replyCcEmails` | string | Comma-separated list of email addresses to CC on prospect reply emails for internal tracking. |
| `replyCount` | number | Total number of replies received across all campaign emails. |
| `replyToEmail` | string | Reply-to email address for prospect responses; must be valid email format with maximum 128 characters. |
| `scheduleSending` | boolean | Enable scheduled sending to control when campaign emails are sent during the day. |
| `scheduleSendOnDate` | date | Specific date to start sending this campaign when scheduled sending is enabled. |
| `scheduleSendOnDateEnabled` | boolean | Enable the scheduled send date feature to start campaign on a specific date. |
| `scheduleSendOnDateHours` | number | Hour of the day (0-23) to start sending on the scheduled date when enabled. |
| `scheduleSendOnDateMinutes` | number | Time of day in minutes after midnight to start sending on the scheduled date; must be between 0 and 1,439 (11:59 PM). |
| `scheduleTimeZone` | string | Timezone identifier for scheduling campaign sends (e.g., 'America/New_York', 'Europe/London'); maximum 64 characters. |
| `sendFri` | boolean | Enable sending campaign emails on Friday. |
| `sendFriAfter` | number | Start time in minutes after midnight for sending emails on Friday; must be between 0 and 1,439 (11:59 PM). |
| `sendFriBefore` | number | End time in minutes after midnight for sending emails on Friday; must be between 0 and 1,439 (11:59 PM). |
| `sendMon` | boolean | Enable sending campaign emails on Monday. |
| `sendMonAfter` | number | Start time in minutes after midnight for sending emails on Monday; must be between 0 and 1,439 (11:59 PM). |
| `sendMonBefore` | number | End time in minutes after midnight for sending emails on Monday; must be between 0 and 1,439 (11:59 PM). |
| `sendSat` | boolean | Enable sending campaign emails on Saturday. |
| `sendSatAfter` | number | Start time in minutes after midnight for sending emails on Saturday; must be between 0 and 1,439 (11:59 PM). |
| `sendSatBefore` | number | End time in minutes after midnight for sending emails on Saturday; must be between 0 and 1,439 (11:59 PM). |
| `sendSun` | boolean | Enable sending campaign emails on Sunday. |
| `sendSunAfter` | number | Start time in minutes after midnight for sending emails on Sunday; must be between 0 and 1,439 (11:59 PM). |
| `sendSunBefore` | number | End time in minutes after midnight for sending emails on Sunday; must be between 0 and 1,439 (11:59 PM). |
| `sendThu` | boolean | Enable sending campaign emails on Thursday. |
| `sendThuAfter` | number | Start time in minutes after midnight for sending emails on Thursday; must be between 0 and 1,439 (11:59 PM). |
| `sendThuBefore` | number | End time in minutes after midnight for sending emails on Thursday; must be between 0 and 1,439 (11:59 PM). |
| `sendTue` | boolean | Enable sending campaign emails on Tuesday. |
| `sendTueAfter` | number | Start time in minutes after midnight for sending emails on Tuesday; must be between 0 and 1,439 (11:59 PM). |
| `sendTueBefore` | number | End time in minutes after midnight for sending emails on Tuesday; must be between 0 and 1,439 (11:59 PM). |
| `sendUnsubscribeListHeader` | boolean | Include List-Unsubscribe email header for compliance with email client unsubscribe features. |
| `sendWed` | boolean | Enable sending campaign emails on Wednesday. |
| `sendWedAfter` | number | Start time in minutes after midnight for sending emails on Wednesday; must be between 0 and 1,439 (11:59 PM). |
| `sendWedBefore` | number | End time in minutes after midnight for sending emails on Wednesday; must be between 0 and 1,439 (11:59 PM). |
| `sentCount` | number | Total number of emails sent across all followups in this campaign. |
| `status` | string | Current campaign status (e.g., 'draft', 'active', 'paused', 'completed'). |
| `stopCoworkersOnReply` | boolean | Stop sending campaign emails to other team members (coworkers) targeting the same prospect when one receives a reply. |
| `subject` | string | Email subject line for the initial campaign email; maximum 4,000 characters. |
| `textOnlyEmails` | boolean | Send emails in plain text format only without HTML formatting. |
| `trackClicks` | boolean | Enable tracking of link clicks by replacing URLs with tracking redirects. |
| `trackOpens` | boolean | Enable tracking of email opens using pixel tracking. |
| `useProspectsTimeZone` | boolean | Enable feature to try and use prospects timezone when available. |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/campaigns/:id` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

