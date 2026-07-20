# Referral Rock: Create Member

Creates a new member in Referral Rock.

```
POST https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "programId": "string",
  "firstName": "Ava",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "programId": "string",
    "firstName": "Ava",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shouldSendEmail` | boolean | no | Send the program confirmation email to the new member. |
| `programId` | string | yes | The ID of the referral program to add the member to. |
| `recruiterSourceId` | string | no | Required when recruiterAssignedId is supplied. |
| `firstName` | string | yes |  |
| `lastName` | string | no |  |
| `email` | string | yes |  |
| `referralCode` | string | no |  |
| `phone` | string | no |  |
| `externalIdentifier` | string | no | Alternative ID used to link the member to external systems. |
| `dateOfBirth` | date | no |  |
| `addressLine1` | string | no |  |
| `addressLine2` | string | no |  |
| `city` | string | no |  |
| `countrySubdivision` | string | no | A country subdivision such as a state or province. |
| `country` | string | no |  |
| `postalCode` | string | no |  |
| `password` | string | no |  |
| `disabledFlag` | boolean | no | Set this when the member should not be enabled for referral programs. |
| `payoutInfo` | object | no | Optional payout details for the member. |
| `payoutInfo.payoutType` | string | no |  |
| `payoutInfo.useDefaultValues` | boolean | no |  |
| `payoutInfo.email` | string | no |  |
| `customOption1Name` | string | no |  |
| `customOption1Value` | string | no |  |
| `customText1Name` | string | no |  |
| `customText1Value` | string | no |  |
| `customText2Name` | string | no |  |
| `customText2Value` | string | no |  |
| `customOverrideURL` | string | no |  |
| `recruiterAssignedId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "member": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `member` | object |  |
| `message` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `POST /api/members` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-member.md) for the provider-specific parameters and requirements.

