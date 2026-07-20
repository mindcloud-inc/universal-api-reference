# Referral Rock: Update Rewards

Updates existing rewards in Referral Rock.

```
PUT https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/update-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/update-rewards" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[].rewardId": "string",
  "items[].payoutId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/update-rewards', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[].rewardId": "string",
    "items[].payoutId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | no |  |
| `items[].description` | string | no |  |
| `items[].rewardId` | string | yes |  |
| `items[].amount` | number | no |  |
| `items[].payoutId` | string | yes |  |
| `items[].eligibilityDate` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resultInfo": {
        "message": {},
        "status": "string"
      },
      "reward": {
        "amount": 1,
        "completeNote": "string",
        "createDate": "string",
        "currencyCode": "string",
        "description": "string",
        "eligibilityDate": "string",
        "externalIdentifier": {},
        "id": "string",
        "issueDate": {},
        "memberId": "string",
        "paymentCode": {},
        "paymentType": {},
        "payoutDescription": "string",
        "payoutId": "string",
        "programId": "string",
        "programName": "Ava Chen",
        "programRewardRuleId": {},
        "reason": {},
        "reasonOther": {},
        "recipientEmailAddress": "ava@example.com",
        "recipientExternalIdentifier": "string",
        "recipientId": "string",
        "recipientName": "Ava Chen",
        "referralDisplayName": {},
        "referralId": {},
        "source": "string",
        "status": "string",
        "transactionID": {},
        "type": "string",
        "updateDate": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultInfo.message` | object |  |
| `resultInfo.status` | string |  |
| `reward.amount` | number |  |
| `reward.completeNote` | string |  |
| `reward.createDate` | string |  |
| `reward.currencyCode` | string |  |
| `reward.description` | string |  |
| `reward.eligibilityDate` | string |  |
| `reward.externalIdentifier` | object |  |
| `reward.id` | string |  |
| `reward.issueDate` | object |  |
| `reward.memberId` | string |  |
| `reward.paymentCode` | object |  |
| `reward.paymentType` | object |  |
| `reward.payoutDescription` | string |  |
| `reward.payoutId` | string |  |
| `reward.programId` | string |  |
| `reward.programName` | string |  |
| `reward.programRewardRuleId` | object |  |
| `reward.reason` | object |  |
| `reward.reasonOther` | object |  |
| `reward.recipientEmailAddress` | string |  |
| `reward.recipientExternalIdentifier` | string |  |
| `reward.recipientId` | string |  |
| `reward.recipientName` | string |  |
| `reward.referralDisplayName` | object |  |
| `reward.referralId` | object |  |
| `reward.source` | string |  |
| `reward.status` | string |  |
| `reward.transactionID` | object |  |
| `reward.type` | string |  |
| `reward.updateDate` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `POST /api/rewards/update` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-rewards.md) for the provider-specific parameters and requirements.

