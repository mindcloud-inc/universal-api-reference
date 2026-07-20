# Referral Rock: Issue Reward

Issues a specific reward in Referral Rock.

```
PUT https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/issue-reward
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/issue-reward" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rewardId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/issue-reward', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rewardId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `overrideIneligible` | boolean | no | Allows issuing rewards with eligibility dates in the future. |
| `rewardId` | string | yes | The unique ID of the reward to issue. |
| `recipientInfo` | string | no | Deprecated extra recipient info; for PayPal this can include the recipient email address. |
| `note` | string | no | Message to send to the reward recipient. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resultInfo": {
        "message": "string",
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
        "issueDate": "string",
        "memberId": "string",
        "paymentCode": "string",
        "paymentType": "string",
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
        "transactionID": "string",
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
| `resultInfo.message` | string |  |
| `resultInfo.status` | string |  |
| `reward.amount` | number |  |
| `reward.completeNote` | string |  |
| `reward.createDate` | string |  |
| `reward.currencyCode` | string |  |
| `reward.description` | string |  |
| `reward.eligibilityDate` | string |  |
| `reward.externalIdentifier` | object |  |
| `reward.id` | string |  |
| `reward.issueDate` | string |  |
| `reward.memberId` | string |  |
| `reward.paymentCode` | string |  |
| `reward.paymentType` | string |  |
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
| `reward.transactionID` | string |  |
| `reward.type` | string |  |
| `reward.updateDate` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `POST /api/rewards/issue` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/issue-reward.md) for the provider-specific parameters and requirements.

