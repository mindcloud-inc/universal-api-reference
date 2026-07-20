# Referral Rock: Get Referral

Retrieves a referral from Referral Rock by email, referral ID, or external ID.

```
GET https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/get-referral
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/get-referral?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/get-referral?${params}`, {
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
| `email` | string | no | The email address of the referral. |
| `externalId` | string | no | The external identifier of the referral. |
| `referralId` | string | no | The unique identifier of the referral. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createDate": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "externalIdentifier": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "memberReferralCode": "string",
      "note": "string",
      "programId": "string",
      "programName": "Ava Chen",
      "programTitle": "string",
      "referringMemberId": "string",
      "referringMemberName": "Ava Chen",
      "status": "string",
      "updateDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createDate` | date |  |
| `displayName` | string |  |
| `email` | string |  |
| `externalIdentifier` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `memberReferralCode` | string |  |
| `note` | string |  |
| `programId` | string |  |
| `programName` | string |  |
| `programTitle` | string |  |
| `referringMemberId` | string |  |
| `referringMemberName` | string |  |
| `status` | string |  |
| `updateDate` | date |  |

## Native endpoint

Through the native Referral Rock API, this operation is `GET /api/referral/single` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-referral.md) for the provider-specific parameters and requirements.

