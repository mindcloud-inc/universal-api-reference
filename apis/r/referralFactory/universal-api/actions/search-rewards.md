# Referral Factory: Search Rewards

Finds rewards in Referral Factory by metric.

```
GET https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Factory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-rewards?connectionId=$CONNECTION_ID&metric=coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "metric": "coupon"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-rewards?${params}`, {
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
| `metric` | string | yes | Reward dashboard metric to search. Example: `coupon`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "coupon": "string",
      "id": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Reward count when the selected metric is not coupon. |
| `coupon` | string | Coupon value when the selected metric is coupon. |
| `id` | number | Referral Factory reward identifier. |
| `total` | number | Reward total when the selected metric is not coupon. |

## Native endpoint

Through the native Referral Factory API, this operation is `POST /rewards/dashboard/:metric/search` (base URL `https://referral-factory.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-rewards.md) for the provider-specific parameters and requirements.

