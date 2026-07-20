# ManyReach: Update Campaign

Updates an existing campaign in ManyReach.

```
PUT https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | HTML email body for the initial campaign message. |
| `description` | string | no | Campaign description. |
| `id` | string | yes | The ID of the campaign to update. |
| `name` | string | no | Campaign display name. |
| `subject` | string | no | Email subject line for the initial campaign email. |

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
| `activeProspectCount` | number |  |
| `bccEmails` | string |  |
| `body` | string |  |
| `bounceCount` | number |  |
| `campaignId` | number |  |
| `ccEmails` | string |  |
| `clickCount` | number |  |
| `conversionCount` | number |  |
| `createdAt` | date |  |
| `dailyLimit` | number |  |
| `dailyLimitIncrease` | boolean |  |
| `dailyLimitIncreasePercent` | number |  |
| `dailyLimitIncreaseToMax` | number |  |
| `dailyLimitInitial` | number |  |
| `dailyLimitInitialEnabled` | boolean |  |
| `dailyLimitOnDate` | date |  |
| `dailyLimitPer` | string |  |
| `dailyLimitPrioritize` | string |  |
| `dailyLimitWhichEmailsCount` | string |  |
| `deactivateIfMissingPlaceholder` | boolean |  |
| `delayMinMinutes` | number |  |
| `description` | string |  |
| `espLimitEnabled` | boolean |  |
| `espLimitToGoogle` | boolean |  |
| `espLimitToMicrosoft` | boolean |  |
| `espLimitToOther` | boolean |  |
| `espMatchEnabled` | boolean |  |
| `espMatchType` | string |  |
| `folderId` | number |  |
| `fromEmails` | string |  |
| `fromName` | string |  |
| `initialBounceCount` | number |  |
| `initialClickCount` | number |  |
| `initialConversionCount` | number |  |
| `initialInterestedCount` | number |  |
| `initialOpenCount` | number |  |
| `initialReplyCount` | number |  |
| `interestedCount` | number |  |
| `name` | string |  |
| `openCount` | number |  |
| `prospectCount` | number |  |
| `prospectValue` | number |  |
| `replyBccEmails` | string |  |
| `replyCcEmails` | string |  |
| `replyCount` | number |  |
| `replyToEmail` | string |  |
| `scheduleSending` | boolean |  |
| `scheduleSendOnDate` | date |  |
| `scheduleSendOnDateEnabled` | boolean |  |
| `scheduleSendOnDateHours` | number |  |
| `scheduleSendOnDateMinutes` | number |  |
| `scheduleTimeZone` | string |  |
| `sendFri` | boolean |  |
| `sendFriAfter` | number |  |
| `sendFriBefore` | number |  |
| `sendMon` | boolean |  |
| `sendMonAfter` | number |  |
| `sendMonBefore` | number |  |
| `sendSat` | boolean |  |
| `sendSatAfter` | number |  |
| `sendSatBefore` | number |  |
| `sendSun` | boolean |  |
| `sendSunAfter` | number |  |
| `sendSunBefore` | number |  |
| `sendThu` | boolean |  |
| `sendThuAfter` | number |  |
| `sendThuBefore` | number |  |
| `sendTue` | boolean |  |
| `sendTueAfter` | number |  |
| `sendTueBefore` | number |  |
| `sendUnsubscribeListHeader` | boolean |  |
| `sendWed` | boolean |  |
| `sendWedAfter` | number |  |
| `sendWedBefore` | number |  |
| `sentCount` | number |  |
| `status` | string |  |
| `stopCoworkersOnReply` | boolean |  |
| `subject` | string |  |
| `textOnlyEmails` | boolean |  |
| `trackClicks` | boolean |  |
| `trackOpens` | boolean |  |
| `useProspectsTimeZone` | boolean |  |

## Native endpoint

Through the native ManyReach API, this operation is `PATCH https://api.manyreach.com/api/v2/campaigns/:id` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

