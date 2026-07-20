# ManyReach: Create Campaign Copy

Creates a copy of a campaign in ManyReach.

```
POST https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-campaign-copy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-campaign-copy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-campaign-copy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeProspectCount": 1,
      "bccEmails": {},
      "body": {},
      "bounceCount": 1,
      "campaignId": 1,
      "ccEmails": {},
      "clickCount": 1,
      "conversionCount": 1,
      "createdAt": "string",
      "dailyLimit": 1,
      "dailyLimitIncrease": true,
      "dailyLimitIncreasePercent": 1,
      "dailyLimitIncreaseToMax": {},
      "dailyLimitInitial": {},
      "dailyLimitInitialEnabled": true,
      "dailyLimitOnDate": {},
      "dailyLimitPer": "string",
      "dailyLimitPrioritize": "string",
      "dailyLimitWhichEmailsCount": "ava@example.com",
      "deactivateIfMissingPlaceholder": true,
      "delayMinMinutes": 1,
      "description": {},
      "espLimitEnabled": true,
      "espLimitToGoogle": true,
      "espLimitToMicrosoft": true,
      "espLimitToOther": true,
      "espMatchEnabled": true,
      "espMatchType": "string",
      "folderId": {},
      "fromEmails": {},
      "fromName": {},
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
      "prospectValue": {},
      "replyBccEmails": {},
      "replyCcEmails": {},
      "replyCount": 1,
      "replyToEmail": {},
      "scheduleSending": true,
      "scheduleSendOnDate": {},
      "scheduleSendOnDateEnabled": {},
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
      "subject": {},
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
| `bccEmails` | object |  |
| `body` | object |  |
| `bounceCount` | number |  |
| `campaignId` | number |  |
| `ccEmails` | object |  |
| `clickCount` | number |  |
| `conversionCount` | number |  |
| `createdAt` | string |  |
| `dailyLimit` | number |  |
| `dailyLimitIncrease` | boolean |  |
| `dailyLimitIncreasePercent` | number |  |
| `dailyLimitIncreaseToMax` | object |  |
| `dailyLimitInitial` | object |  |
| `dailyLimitInitialEnabled` | boolean |  |
| `dailyLimitOnDate` | object |  |
| `dailyLimitPer` | string |  |
| `dailyLimitPrioritize` | string |  |
| `dailyLimitWhichEmailsCount` | string |  |
| `deactivateIfMissingPlaceholder` | boolean |  |
| `delayMinMinutes` | number |  |
| `description` | object |  |
| `espLimitEnabled` | boolean |  |
| `espLimitToGoogle` | boolean |  |
| `espLimitToMicrosoft` | boolean |  |
| `espLimitToOther` | boolean |  |
| `espMatchEnabled` | boolean |  |
| `espMatchType` | string |  |
| `folderId` | object |  |
| `fromEmails` | object |  |
| `fromName` | object |  |
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
| `prospectValue` | object |  |
| `replyBccEmails` | object |  |
| `replyCcEmails` | object |  |
| `replyCount` | number |  |
| `replyToEmail` | object |  |
| `scheduleSending` | boolean |  |
| `scheduleSendOnDate` | object |  |
| `scheduleSendOnDateEnabled` | object |  |
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
| `subject` | object |  |
| `textOnlyEmails` | boolean |  |
| `trackClicks` | boolean |  |
| `trackOpens` | boolean |  |
| `useProspectsTimeZone` | boolean |  |

## Native endpoint

Through the native ManyReach API, this operation is `POST https://api.manyreach.com/api/v2/campaigns/:id/copy` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign-copy.md) for the provider-specific parameters and requirements.

