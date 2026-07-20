# ManyReach: Create Sender

Creates a new sender in ManyReach.

```
POST https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-sender" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customImapPass": "string",
  "customImapPort": "string",
  "customImapServer": "string",
  "customSmtpPass": "string",
  "customSmtpPort": 1,
  "customSmtpServer": "string",
  "dailyLimit": 1,
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-sender', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customImapPass": "string",
    "customImapPort": "string",
    "customImapServer": "string",
    "customSmtpPass": "string",
    "customSmtpPort": 1,
    "customSmtpServer": "string",
    "dailyLimit": 1,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customImapPass` | string | yes | IMAP password. |
| `customImapPort` | string | yes | IMAP server port. |
| `customImapServer` | string | yes | IMAP server hostname. |
| `customImapUsername` | string | no | IMAP username. |
| `customSmtpPass` | string | yes | SMTP password. |
| `customSmtpPort` | number | yes | SMTP server port. |
| `customSmtpServer` | string | yes | SMTP server hostname. |
| `customSmtpUsername` | string | no | SMTP username. |
| `customWarmupTag` | string | no | Custom tag applied to warmup behavior. |
| `dailyLimit` | number | yes | Maximum emails the sender can send per day. |
| `dailyLimitIncrease` | boolean | no | Whether the daily limit increases automatically. |
| `dailyLimitIncreasePercent` | number | no | Percentage increase applied to the daily limit. |
| `dailyLimitIncreaseToMax` | number | no | Maximum daily limit when automatic increases are enabled. |
| `delayMin` | number | no | Delay in minutes between sent emails. |
| `email` | string | yes | Sender email address. |
| `firstName` | string | no | Sender first name. |
| `folder` | string | no | Folder used to organize the sender. |
| `fromName` | string | no | Display name shown in outgoing emails. |
| `lastName` | string | no | Sender last name. |
| `replyTo` | string | no | Reply-to email address. |
| `senderCustom1` | string | no | Custom sender field 1. |
| `senderCustom10` | string | no | Custom sender field 10. |
| `senderCustom2` | string | no | Custom sender field 2. |
| `senderCustom3` | string | no | Custom sender field 3. |
| `senderCustom4` | string | no | Custom sender field 4. |
| `senderCustom5` | string | no | Custom sender field 5. |
| `senderCustom6` | string | no | Custom sender field 6. |
| `senderCustom7` | string | no | Custom sender field 7. |
| `senderCustom8` | string | no | Custom sender field 8. |
| `senderCustom9` | string | no | Custom sender field 9. |
| `signature` | string | no | Email signature HTML. |
| `trackingDomain` | string | no | Custom tracking domain for the sender. |
| `warmup` | boolean | no | Whether sender warmup is enabled. |
| `warmupDailyLimit` | number | no | Daily sending limit used during warmup. |
| `warmupDailyLimitIncrease` | boolean | no | Whether the warmup daily limit increases automatically. |
| `warmupDailyLimitIncreasePercent` | number | no | Percentage increase applied to the warmup daily limit. |
| `warmupDailyLimitIncreaseToMax` | number | no | Maximum warmup daily limit when automatic increases are enabled. |
| `warmupReplyPercent` | number | no | Expected reply percentage during warmup. |
| `warmupSkipWeekends` | boolean | no | Whether warmup activity skips weekends. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customImapPort": "string",
      "customImapServer": "string",
      "customImapUsername": "Ava Chen",
      "customSmtpPort": 1,
      "customSmtpServer": "string",
      "customSmtpUsername": "Ava Chen",
      "customWarmupTag": "string",
      "dailyLimit": 1,
      "dailyLimitIncrease": true,
      "dailyLimitIncreasePercent": 1,
      "dailyLimitIncreaseToMax": 1,
      "dateDisconnected": "2026-05-07T12:00:00.000Z",
      "dateWarmupDisconnected": "2026-05-07T12:00:00.000Z",
      "delayMin": 1,
      "disconnected": true,
      "disconnectionReason": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "folder": "string",
      "fromName": "Ava Chen",
      "lastName": "Chen",
      "replyTo": "string",
      "senderCustom1": "string",
      "senderCustom10": "string",
      "senderCustom2": "string",
      "senderCustom3": "string",
      "senderCustom4": "string",
      "senderCustom5": "string",
      "senderCustom6": "string",
      "senderCustom7": "string",
      "senderCustom8": "string",
      "senderCustom9": "string",
      "senderId": 1,
      "signature": "string",
      "trackingDomain": "string",
      "warmup": true,
      "warmupDailyLimit": 1,
      "warmupDailyLimitIncrease": true,
      "warmupDailyLimitIncreasePercent": 1,
      "warmupDailyLimitIncreaseToMax": 1,
      "warmupRemovalReason": "string",
      "warmupReplyPercent": 1,
      "warmupSkipWeekends": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string |  |
| `createdAt` | date |  |
| `customImapPort` | string |  |
| `customImapServer` | string |  |
| `customImapUsername` | string |  |
| `customSmtpPort` | number |  |
| `customSmtpServer` | string |  |
| `customSmtpUsername` | string |  |
| `customWarmupTag` | string |  |
| `dailyLimit` | number |  |
| `dailyLimitIncrease` | boolean |  |
| `dailyLimitIncreasePercent` | number |  |
| `dailyLimitIncreaseToMax` | number |  |
| `dateDisconnected` | date |  |
| `dateWarmupDisconnected` | date |  |
| `delayMin` | number |  |
| `disconnected` | boolean |  |
| `disconnectionReason` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `folder` | string |  |
| `fromName` | string |  |
| `lastName` | string |  |
| `replyTo` | string |  |
| `senderCustom1` | string |  |
| `senderCustom10` | string |  |
| `senderCustom2` | string |  |
| `senderCustom3` | string |  |
| `senderCustom4` | string |  |
| `senderCustom5` | string |  |
| `senderCustom6` | string |  |
| `senderCustom7` | string |  |
| `senderCustom8` | string |  |
| `senderCustom9` | string |  |
| `senderId` | number |  |
| `signature` | string |  |
| `trackingDomain` | string |  |
| `warmup` | boolean |  |
| `warmupDailyLimit` | number |  |
| `warmupDailyLimitIncrease` | boolean |  |
| `warmupDailyLimitIncreasePercent` | number |  |
| `warmupDailyLimitIncreaseToMax` | number |  |
| `warmupRemovalReason` | string |  |
| `warmupReplyPercent` | number |  |
| `warmupSkipWeekends` | boolean |  |

## Native endpoint

Through the native ManyReach API, this operation is `POST https://api.manyreach.com/api/v2/senders` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sender.md) for the provider-specific parameters and requirements.

