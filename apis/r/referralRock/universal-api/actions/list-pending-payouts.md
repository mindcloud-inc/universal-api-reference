# Referral Rock: List Pending Payouts

Retrieves pending payouts from Referral Rock.

```
GET https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-pending-payouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-pending-payouts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-pending-payouts?${params}`, {
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
| `includeIneligible` | boolean | no | Include payouts for rewards with future eligibility dates. |
| `memberId` | string | no | The unique ID of the member to whom the amount is owed. Deprecated. |
| `recipientId` | string | no | The unique ID of the recipient to whom the amount is owed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "Description": "string",
      "memberId": "string",
      "memberName": "Ava Chen",
      "payoutId": "string",
      "recipientId": "string",
      "RecipientName": "Ava Chen",
      "RecipientType": "string",
      "rewardCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `Description` | string |  |
| `memberId` | string |  |
| `memberName` | string |  |
| `payoutId` | string |  |
| `recipientId` | string |  |
| `RecipientName` | string |  |
| `RecipientType` | string |  |
| `rewardCount` | number |  |

## Native endpoint

Through the native Referral Rock API, this operation is `GET /api/payouts/pending` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pending-payouts.md) for the provider-specific parameters and requirements.

