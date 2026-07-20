# Referral Rock: List Members

Retrieves referral program members from Referral Rock.

```
GET https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-members?${params}`, {
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
| `dateFrom` | date | no | Show members created after this date. |
| `dateTo` | date | no | Show members created before this date. |
| `programId` | string | no | ID of the program, program name, or program title. |
| `query` | string | no | Filter members by email, internal ID, external ID, or referral code. |
| `showDisabled` | boolean | no | Set true to include disabled members. |
| `sort` | string | no | Column to sort by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activatedDate": "2026-05-07T12:00:00.000Z",
      "createDt": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "externalIdentifier": "string",
      "firstName": "Ava",
      "id": "string",
      "lastActiveDate": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "memberUrl": "https://example.com",
      "programId": "string",
      "programName": "Ava Chen",
      "programTitle": "string",
      "referralCode": "string",
      "referralUrl": "https://example.com",
      "rewardAmountTotal": 1,
      "rewards": 1,
      "rewardsIssuedAmount": 1,
      "rewardsPendingAmount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activatedDate` | date |  |
| `createDt` | date |  |
| `displayName` | string |  |
| `email` | string |  |
| `externalIdentifier` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastActiveDate` | date |  |
| `lastName` | string |  |
| `memberUrl` | string |  |
| `programId` | string |  |
| `programName` | string |  |
| `programTitle` | string |  |
| `referralCode` | string |  |
| `referralUrl` | string |  |
| `rewardAmountTotal` | number |  |
| `rewards` | number |  |
| `rewardsIssuedAmount` | number |  |
| `rewardsPendingAmount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `GET /api/members` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

