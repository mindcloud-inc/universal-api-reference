# Referral Rock: Create Referral

Creates a new referral in Referral Rock from a member referral code.

```
POST https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-referral
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-referral" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "referralCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-referral', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "referralCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `referralCode` | string | yes | Referral code from the member who introduced the referral. |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `email` | string | no |  |
| `phoneNumber` | string | no |  |
| `preferredContact` | string | no | Allowed values are email, callMorning, callAfternoon, or callEvening. |
| `externalIdentifier` | string | no | Unique external ID you can use to reference the referral later. |
| `amount` | number | no | Passed order amount or total. |
| `companyName` | string | no |  |
| `note` | string | no |  |
| `publicNote` | string | no |  |
| `customOption1Name` | string | no |  |
| `customOption2Name` | string | no |  |
| `customText1Name` | string | no |  |
| `customText2Name` | string | no |  |
| `customText3Name` | string | no |  |
| `customOption1Value` | string | no |  |
| `customOption2Value` | string | no |  |
| `customText1Value` | string | no |  |
| `customText2Value` | string | no |  |
| `customText3Value` | string | no |  |
| `status` | string | no | Allowed values are pending, qualified, approved, or denied. |
| `addressLine1` | string | no |  |
| `addressLine2` | string | no |  |
| `city` | string | no |  |
| `region` | string | no | Must be a region name or ISO 3166-2 subdivision code, and can only be supplied if country is also provided. |
| `postalCode` | string | no |  |
| `country` | string | no | Referral country name or ISO 3166-2 country code. |
| `recruiterAssignedId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "referral": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `referral` | object |  |

## Native endpoint

Through the native Referral Rock API, this operation is `POST /api/referrals` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-referral.md) for the provider-specific parameters and requirements.

