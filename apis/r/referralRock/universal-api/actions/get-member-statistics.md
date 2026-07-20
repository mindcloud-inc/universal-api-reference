# Referral Rock: Get Member Statistics

Retrieves member sharing and reward statistics from Referral Rock.

```
GET https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/get-member-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/get-member-statistics?connectionId=$CONNECTION_ID&query=string&timePeriod=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "timePeriod": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/get-member-statistics?${params}`, {
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
| `query` | string | yes | A member email address, ID, external ID, or referral code. |
| `timePeriod` | string | yes | One of All, MonthToDate, LastMonth, Last7Days, or Last30Days. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activatedDate": "2026-05-07T12:00:00.000Z",
      "lastActiveDate": "2026-05-07T12:00:00.000Z",
      "memberShares": 1,
      "memberViews": 1,
      "referralsApproved": 1,
      "referralsCount": 1,
      "referralsPending": 1,
      "referralsQualified": 1,
      "rewardAmountTotal": 1,
      "rewardsCount": 1,
      "rewardsIssuedAmount": 1,
      "rewardsPendingAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activatedDate` | date |  |
| `lastActiveDate` | date |  |
| `memberShares` | number |  |
| `memberViews` | number |  |
| `referralsApproved` | number |  |
| `referralsCount` | number |  |
| `referralsPending` | number |  |
| `referralsQualified` | number |  |
| `rewardAmountTotal` | number |  |
| `rewardsCount` | number |  |
| `rewardsIssuedAmount` | number |  |
| `rewardsPendingAmount` | number |  |

## Native endpoint

Through the native Referral Rock API, this operation is `GET /api/memberstats/getsingle` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member-statistics.md) for the provider-specific parameters and requirements.

