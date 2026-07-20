# Referral Rock: Update Referrals

Updates existing referrals in Referral Rock.

```
PUT https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/update-referrals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/update-referrals" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[].query": {},
  "items[].referral": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/update-referrals', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[].query": {},
    "items[].referral": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | no |  |
| `items[].query.fuzzyInfo.identifier` | string | no |  |
| `items[].query.primaryInfo.referralId` | string | no |  |
| `items[].query.secondaryInfo.email` | string | no |  |
| `items[].query.secondaryInfo.externalIdentifier` | string | no |  |
| `items[].query.secondaryInfo.phoneNumber` | string | no |  |
| `items[].query.tertiaryInfo.programId` | string | no |  |
| `items[].query.tertiaryInfo.programName` | string | no |  |
| `items[].query.tertiaryInfo.programTitle` | string | no |  |
| `items[].referral.companyName` | string | no |  |
| `items[].referral.customOption1Name` | string | no |  |
| `items[].referral.customOption2Name` | string | no |  |
| `items[].referral.customText1Name` | string | no |  |
| `items[].referral.customText2Name` | string | no |  |
| `items[].referral.customText3Name` | string | no |  |
| `items[].referral.email` | string | no |  |
| `items[].referral.externalIdentifier` | string | no |  |
| `items[].referral.firstName` | string | no |  |
| `items[].referral.lastName` | string | no |  |
| `items[].referral.note` | string | no |  |
| `items[].referral.phoneNumber` | string | no |  |
| `items[].referral.preferredContact` | string | no |  |
| `items[].referral.publicNote` | string | no |  |
| `items[].query` | object | yes |  |
| `items[].query.primaryInfo` | object | no |  |
| `items[].query.secondaryInfo` | object | no |  |
| `items[].query.tertiaryInfo` | object | no |  |
| `items[].query.fuzzyInfo` | object | no |  |
| `items[].referral` | object | yes |  |
| `items[].referral.amount` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "query": {
        "fuzzyInfo": {},
        "primaryInfo": {
          "referralId": "string"
        },
        "secondaryInfo": {},
        "tertiaryInfo": {}
      },
      "referral": {
        "addressLine1": {},
        "addressLine2": {},
        "amount": 1,
        "amountFormatted": "string",
        "approvedDate": {},
        "browserReferrerUrl": "https://example.com",
        "city": {},
        "companyName": "Ava Chen",
        "conversionIPAddress": "string",
        "conversionNote": "string",
        "country": {},
        "createDate": "string",
        "customOption1Name": "Ava Chen",
        "customOption1Value": "string",
        "customOption2Name": "Ava Chen",
        "customOption2Value": "string",
        "customText1Name": "Ava Chen",
        "customText1Value": "string",
        "customText2Name": "Ava Chen",
        "customText2Value": "string",
        "customText3Name": "Ava Chen",
        "customText3Value": "string",
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "externalIdentifier": "string",
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "id": "string",
        "iPAddressSource": "string",
        "lastName": "Chen",
        "memberEmail": "ava@example.com",
        "memberExternalIdentifier": "string",
        "memberReferralCode": "string",
        "note": "string",
        "phoneNumber": "string",
        "postalCode": {},
        "preferredContact": "string",
        "programId": "string",
        "programName": "Ava Chen",
        "programTitle": "string",
        "publicNote": "string",
        "qualifiedDate": {},
        "recruiterAssignedEmail": "ava@example.com",
        "recruiterAssignedExternalId": {},
        "recruiterAssignedId": {},
        "recruiterAssignedName": "Ava Chen",
        "recruiterSourceEmail": "ava@example.com",
        "recruiterSourceExternalId": {},
        "recruiterSourceId": {},
        "recruiterSourceName": "Ava Chen",
        "referringMemberId": "string",
        "referringMemberName": "Ava Chen",
        "region": {},
        "source": "string",
        "status": "string",
        "updateDate": "string",
        "utmCampaign": "string",
        "utmMedium": "string",
        "utmSource": "string"
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
| `query.fuzzyInfo` | object |  |
| `query.primaryInfo.referralId` | string |  |
| `query.secondaryInfo` | object |  |
| `query.tertiaryInfo` | object |  |
| `referral.addressLine1` | object |  |
| `referral.addressLine2` | object |  |
| `referral.amount` | number |  |
| `referral.amountFormatted` | string |  |
| `referral.approvedDate` | object |  |
| `referral.browserReferrerUrl` | string |  |
| `referral.city` | object |  |
| `referral.companyName` | string |  |
| `referral.conversionIPAddress` | string |  |
| `referral.conversionNote` | string |  |
| `referral.country` | object |  |
| `referral.createDate` | string |  |
| `referral.customOption1Name` | string |  |
| `referral.customOption1Value` | string |  |
| `referral.customOption2Name` | string |  |
| `referral.customOption2Value` | string |  |
| `referral.customText1Name` | string |  |
| `referral.customText1Value` | string |  |
| `referral.customText2Name` | string |  |
| `referral.customText2Value` | string |  |
| `referral.customText3Name` | string |  |
| `referral.customText3Value` | string |  |
| `referral.displayName` | string |  |
| `referral.email` | string |  |
| `referral.externalIdentifier` | string |  |
| `referral.firstName` | string |  |
| `referral.fullName` | string |  |
| `referral.id` | string |  |
| `referral.iPAddressSource` | string |  |
| `referral.lastName` | string |  |
| `referral.memberEmail` | string |  |
| `referral.memberExternalIdentifier` | string |  |
| `referral.memberReferralCode` | string |  |
| `referral.note` | string |  |
| `referral.phoneNumber` | string |  |
| `referral.postalCode` | object |  |
| `referral.preferredContact` | string |  |
| `referral.programId` | string |  |
| `referral.programName` | string |  |
| `referral.programTitle` | string |  |
| `referral.publicNote` | string |  |
| `referral.qualifiedDate` | object |  |
| `referral.recruiterAssignedEmail` | string |  |
| `referral.recruiterAssignedExternalId` | object |  |
| `referral.recruiterAssignedId` | object |  |
| `referral.recruiterAssignedName` | string |  |
| `referral.recruiterSourceEmail` | string |  |
| `referral.recruiterSourceExternalId` | object |  |
| `referral.recruiterSourceId` | object |  |
| `referral.recruiterSourceName` | string |  |
| `referral.referringMemberId` | string |  |
| `referral.referringMemberName` | string |  |
| `referral.region` | object |  |
| `referral.source` | string |  |
| `referral.status` | string |  |
| `referral.updateDate` | string |  |
| `referral.utmCampaign` | string |  |
| `referral.utmMedium` | string |  |
| `referral.utmSource` | string |  |
| `resultInfo.message` | string |  |
| `resultInfo.status` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `POST /api/referral/update` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-referrals.md) for the provider-specific parameters and requirements.

