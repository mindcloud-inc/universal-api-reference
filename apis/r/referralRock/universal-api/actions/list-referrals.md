# Referral Rock: List Referrals

Retrieves referral records from Referral Rock.

```
GET https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-referrals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-referrals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-referrals?${params}`, {
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
| `dateFrom` | date | no | Show referrals created after this date. |
| `dateTo` | date | no | Show referrals created before this date. |
| `memberId` | string | no | Filter referrals by member ID. |
| `programId` | string | no | ID of the program, program name, or program title. |
| `query` | string | no | Filter referrals by email, internal ID, external ID, or referral code. |
| `sort` | string | no | Column to sort by. |
| `status` | string | no | Filter referrals by status: pending, qualified, approved, or denied. |

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

Through the native Referral Rock API, this operation is `GET /api/referrals` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-referrals.md) for the provider-specific parameters and requirements.

