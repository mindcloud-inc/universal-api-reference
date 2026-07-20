# Referral Factory: List Issued Rewards

Retrieves issued rewards from Referral Factory by metric.

```
GET https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/list-issued-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Factory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/list-issued-rewards?connectionId=$CONNECTION_ID&metric=coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "metric": "coupon"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/list-issued-rewards?${params}`, {
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
| `metric` | string | yes | Issued reward dashboard metric to retrieve. Example: `coupon`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "coupon": "string",
      "id": 1,
      "issued_at": "2026-05-07T12:00:00.000Z",
      "recipient_id": 1,
      "reward_id": 1,
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Reward count when the reward metric is not coupon. |
| `coupon` | string | Coupon code when the reward metric is coupon. |
| `id` | number | Referral Factory issued reward identifier. |
| `issued_at` | date | Date the reward was issued. |
| `recipient_id` | number | Recipient user identifier. |
| `reward_id` | number | Reward definition identifier. |
| `status` | string | Issued reward status. |
| `total` | number | Reward total when the reward metric is not coupon. |

## Native endpoint

Through the native Referral Factory API, this operation is `GET /rewards/issued/:metric` (base URL `https://referral-factory.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-issued-rewards.md) for the provider-specific parameters and requirements.

