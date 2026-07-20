# ManyReach: Get Sender

Retrieves a sender from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-sender?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-sender?${params}`, {
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
| `id` | string | yes | The ID of the sender to retrieve. |

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

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/senders/:id` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sender.md) for the provider-specific parameters and requirements.

