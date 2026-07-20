# Referral Rock: List Rewards

Retrieves reward records from Referral Rock.

```
GET https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-rewards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-rewards?${params}`, {
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
| `dateFrom` | date | no | Show rewards created after this date. |
| `dateTo` | date | no | Show rewards created before this date. |
| `memberId` | string | no | ID of the member. |
| `programId` | string | no | ID of the program, program name, or program title. |
| `query` | string | no | Filter the recipient by email, ID, external ID, or member referral code. |
| `sort` | string | no | Column to sort by. |
| `status` | string | no | Filter rewards by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "completeNote": "string",
      "createDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "eligibilityDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "issueDate": "2026-05-07T12:00:00.000Z",
      "memberId": "string",
      "paymentCode": "string",
      "paymentType": "string",
      "payoutDescription": "string",
      "payoutId": "string",
      "programId": "string",
      "programName": "Ava Chen",
      "recipientEmailAddress": "ava@example.com",
      "recipientExternalIdentifier": "string",
      "recipientId": "string",
      "recipientName": "Ava Chen",
      "status": "string",
      "transactionID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `completeNote` | string |  |
| `createDate` | date |  |
| `description` | string |  |
| `eligibilityDate` | date |  |
| `id` | string |  |
| `issueDate` | date |  |
| `memberId` | string |  |
| `paymentCode` | string |  |
| `paymentType` | string |  |
| `payoutDescription` | string |  |
| `payoutId` | string |  |
| `programId` | string |  |
| `programName` | string |  |
| `recipientEmailAddress` | string |  |
| `recipientExternalIdentifier` | string |  |
| `recipientId` | string |  |
| `recipientName` | string |  |
| `status` | string |  |
| `transactionID` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `GET /api/rewards` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rewards.md) for the provider-specific parameters and requirements.

