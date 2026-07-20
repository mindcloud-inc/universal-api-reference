# Referral Rock: Update Members

Updates existing members in Referral Rock.

```
PUT https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/update-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/update-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[].query": {},
  "items[].member": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/update-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[].query": {},
    "items[].member": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | no |  |
| `items[].member.addressLine1` | string | no |  |
| `items[].member.addressLine2` | string | no |  |
| `items[].member.city` | string | no |  |
| `items[].member.country` | string | no |  |
| `items[].member.countrySubdivision` | string | no |  |
| `items[].member.customOption1Name` | string | no |  |
| `items[].member.customOption1Value` | string | no |  |
| `items[].member.customOverrideURL` | string | no |  |
| `items[].member.customText1Name` | string | no |  |
| `items[].member.customText1Value` | string | no |  |
| `items[].member.customText2Name` | string | no |  |
| `items[].member.customText2Value` | string | no |  |
| `items[].member.email` | string | no |  |
| `items[].member.externalIdentifier` | string | no |  |
| `items[].member.firstName` | string | no |  |
| `items[].member.lastName` | string | no |  |
| `items[].member.password` | string | no |  |
| `items[].member.payoutInfo.email` | string | no |  |
| `items[].member.payoutInfo.payoutType` | string | no |  |
| `items[].member.phone` | string | no |  |
| `items[].member.postalCode` | string | no |  |
| `items[].member.recruiterAssignedId` | string | no |  |
| `items[].member.referralCode` | string | no |  |
| `items[].member.region` | string | no |  |
| `items[].query.primaryInfo.memberId` | string | no |  |
| `items[].query.primaryInfo.referralCode` | string | no |  |
| `items[].query.secondaryInfo.email` | string | no |  |
| `items[].query.secondaryInfo.externalIdentifier` | string | no |  |
| `items[].query.tertiaryInfo.programId` | string | no |  |
| `items[].query.tertiaryInfo.programName` | string | no |  |
| `items[].query.tertiaryInfo.programTitle` | string | no |  |
| `items[].query` | object | yes |  |
| `items[].query.primaryInfo` | object | no |  |
| `items[].query.secondaryInfo` | object | no |  |
| `items[].query.tertiaryInfo` | object | no |  |
| `items[].member` | object | yes |  |
| `items[].member.dateOfBirth` | date | no |  |
| `items[].member.disabledFlag` | boolean | no |  |
| `items[].member.payoutInfo` | object | no |  |
| `items[].member.payoutInfo.useDefaultValues` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "member": {
        "activatedDate": {},
        "addressLine1": "string",
        "addressLine2": "string",
        "browserReferrerUrl": "https://example.com",
        "city": "string",
        "country": "string",
        "countrySubdivision": "string",
        "createDt": "string",
        "customOption1Name": "Ava Chen",
        "customOption1Value": "string",
        "customOverrideURL": "https://example.com",
        "customText1Name": "Ava Chen",
        "customText1Value": "string",
        "customText2Name": "Ava Chen",
        "customText2Value": "string",
        "dateOfBirth": {},
        "disabledFlag": true,
        "disabledReason": "string",
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "emailShares": 1,
        "externalIdentifier": "string",
        "firstMemberRewardAddDate": {},
        "firstMemberShareDate": {},
        "firstMemberViewDate": {},
        "firstName": "Ava",
        "firstReferralAddDate": {},
        "firstReferralViewDate": {},
        "id": "string",
        "lastActiveDate": {},
        "lastMemberRewardAddDate": {},
        "lastName": "Chen",
        "lastReferralAddDate": {},
        "lastShare": {},
        "lastViewIPAddress": "string",
        "memberUrl": "https://example.com",
        "payoutInfo": {},
        "phone": "string",
        "postalCode": "string",
        "programId": "string",
        "programName": "Ava Chen",
        "programTitle": "string",
        "recruiterAssignedEmail": "ava@example.com",
        "recruiterAssignedExternalId": {},
        "recruiterAssignedId": {},
        "recruiterAssignedName": "Ava Chen",
        "recruiterSourceEmail": "ava@example.com",
        "recruiterSourceExternalId": {},
        "recruiterSourceId": {},
        "recruiterSourceName": "Ava Chen",
        "referralCode": "string",
        "referrals": 1,
        "referralsApproved": 1,
        "referralsApprovedAmount": 1,
        "referralsPending": 1,
        "referralsQualified": 1,
        "referralUrl": "https://example.com",
        "region": {},
        "rewardAmountTotal": 1,
        "rewards": 1,
        "rewardsIssuedAmount": 1,
        "rewardsPendingAmount": 1,
        "socialShares": 1,
        "status": "string",
        "utmCampaign": "string",
        "utmMedium": "string",
        "utmSource": "string",
        "views": 1
      },
      "query": {
        "primaryInfo": {
          "memberId": "string",
          "referralCode": {}
        },
        "secondaryInfo": {},
        "tertiaryInfo": {}
      },
      "resultInfo": {
        "message": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `member.activatedDate` | object |  |
| `member.addressLine1` | string |  |
| `member.addressLine2` | string |  |
| `member.browserReferrerUrl` | string |  |
| `member.city` | string |  |
| `member.country` | string |  |
| `member.countrySubdivision` | string |  |
| `member.createDt` | string |  |
| `member.customOption1Name` | string |  |
| `member.customOption1Value` | string |  |
| `member.customOverrideURL` | string |  |
| `member.customText1Name` | string |  |
| `member.customText1Value` | string |  |
| `member.customText2Name` | string |  |
| `member.customText2Value` | string |  |
| `member.dateOfBirth` | object |  |
| `member.disabledFlag` | boolean |  |
| `member.disabledReason` | string |  |
| `member.displayName` | string |  |
| `member.email` | string |  |
| `member.emailShares` | number |  |
| `member.externalIdentifier` | string |  |
| `member.firstMemberRewardAddDate` | object |  |
| `member.firstMemberShareDate` | object |  |
| `member.firstMemberViewDate` | object |  |
| `member.firstName` | string |  |
| `member.firstReferralAddDate` | object |  |
| `member.firstReferralViewDate` | object |  |
| `member.id` | string |  |
| `member.lastActiveDate` | object |  |
| `member.lastMemberRewardAddDate` | object |  |
| `member.lastName` | string |  |
| `member.lastReferralAddDate` | object |  |
| `member.lastShare` | object |  |
| `member.lastViewIPAddress` | string |  |
| `member.memberUrl` | string |  |
| `member.payoutInfo` | object |  |
| `member.phone` | string |  |
| `member.postalCode` | string |  |
| `member.programId` | string |  |
| `member.programName` | string |  |
| `member.programTitle` | string |  |
| `member.recruiterAssignedEmail` | string |  |
| `member.recruiterAssignedExternalId` | object |  |
| `member.recruiterAssignedId` | object |  |
| `member.recruiterAssignedName` | string |  |
| `member.recruiterSourceEmail` | string |  |
| `member.recruiterSourceExternalId` | object |  |
| `member.recruiterSourceId` | object |  |
| `member.recruiterSourceName` | string |  |
| `member.referralCode` | string |  |
| `member.referrals` | number |  |
| `member.referralsApproved` | number |  |
| `member.referralsApprovedAmount` | number |  |
| `member.referralsPending` | number |  |
| `member.referralsQualified` | number |  |
| `member.referralUrl` | string |  |
| `member.region` | object |  |
| `member.rewardAmountTotal` | number |  |
| `member.rewards` | number |  |
| `member.rewardsIssuedAmount` | number |  |
| `member.rewardsPendingAmount` | number |  |
| `member.socialShares` | number |  |
| `member.status` | string |  |
| `member.utmCampaign` | string |  |
| `member.utmMedium` | string |  |
| `member.utmSource` | string |  |
| `member.views` | number |  |
| `query.primaryInfo.memberId` | string |  |
| `query.primaryInfo.referralCode` | object |  |
| `query.secondaryInfo` | object |  |
| `query.tertiaryInfo` | object |  |
| `resultInfo.message` | string |  |
| `resultInfo.status` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `POST /api/members/update` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-members.md) for the provider-specific parameters and requirements.

