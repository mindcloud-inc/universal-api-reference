# Referral Factory: Search Due Rewards

Finds due rewards in Referral Factory by metric.

```
GET https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-due-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Factory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-due-rewards?connectionId=$CONNECTION_ID&metric=coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "metric": "coupon"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-due-rewards?${params}`, {
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
| `metric` | string | yes | Due reward dashboard metric to search. Example: `coupon`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "can_be_issued": true,
      "count": 1,
      "coupon": "string",
      "id": 1,
      "recipient_id": 1,
      "reward_id": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can_be_issued` | boolean | Whether the due reward can be issued. |
| `count` | number | Reward count when the reward metric is not coupon. |
| `coupon` | string | Coupon code when the reward metric is coupon. |
| `id` | number | Referral Factory due reward identifier. |
| `recipient_id` | number | Recipient user identifier. |
| `reward_id` | number | Reward definition identifier. |
| `total` | number | Reward total when the reward metric is not coupon. |

## Native endpoint

Through the native Referral Factory API, this operation is `POST /rewards/due/:metric/search` (base URL `https://referral-factory.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-due-rewards.md) for the provider-specific parameters and requirements.

