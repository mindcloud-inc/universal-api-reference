# Referral Rock: Create Rewards

Creates new rewards in Referral Rock.

```
POST https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-rewards" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[].newReward": {},
  "items[].newReward.payoutId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-rewards', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[].newReward": {},
    "items[].newReward.payoutId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | no |  |
| `items[].memberQuery.primaryInfo.memberId` | string | no |  |
| `items[].memberQuery.primaryInfo.referralCode` | string | no |  |
| `items[].memberQuery.secondaryInfo.email` | string | no |  |
| `items[].memberQuery.secondaryInfo.externalIdentifier` | string | no |  |
| `items[].memberQuery.tertiaryInfo.programId` | string | no |  |
| `items[].memberQuery.tertiaryInfo.programName` | string | no |  |
| `items[].memberQuery.tertiaryInfo.programTitle` | string | no |  |
| `items[].newReward.description` | string | no |  |
| `items[].referralQuery.fuzzyInfo.identifier` | string | no |  |
| `items[].referralQuery.primaryInfo.referralId` | string | no |  |
| `items[].referralQuery.secondaryInfo.email` | string | no |  |
| `items[].referralQuery.secondaryInfo.externalIdentifier` | string | no |  |
| `items[].referralQuery.secondaryInfo.phoneNumber` | string | no |  |
| `items[].referralQuery.tertiaryInfo.programId` | string | no |  |
| `items[].referralQuery.tertiaryInfo.programName` | string | no |  |
| `items[].referralQuery.tertiaryInfo.programTitle` | string | no |  |
| `items[].memberQuery` | object | no |  |
| `items[].memberQuery.primaryInfo` | object | no |  |
| `items[].memberQuery.secondaryInfo` | object | no |  |
| `items[].memberQuery.tertiaryInfo` | object | no |  |
| `items[].referralQuery` | object | no |  |
| `items[].referralQuery.primaryInfo` | object | no |  |
| `items[].referralQuery.secondaryInfo` | object | no |  |
| `items[].referralQuery.tertiaryInfo` | object | no |  |
| `items[].referralQuery.fuzzyInfo` | object | no |  |
| `items[].newReward` | object | yes |  |
| `items[].newReward.amount` | number | no |  |
| `items[].newReward.payoutId` | string | yes |  |
| `items[].newReward.eligibilityDate` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "memberQuery": {
        "primaryInfo": {
          "memberId": "string",
          "referralCode": {}
        },
        "secondaryInfo": {},
        "tertiaryInfo": {}
      },
      "referralQuery": {},
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
| `memberQuery.primaryInfo.memberId` | string |  |
| `memberQuery.primaryInfo.referralCode` | object |  |
| `memberQuery.secondaryInfo` | object |  |
| `memberQuery.tertiaryInfo` | object |  |
| `referralQuery` | object |  |
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

Through the native Referral Rock API, this operation is `POST /api/rewards` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-rewards.md) for the provider-specific parameters and requirements.

