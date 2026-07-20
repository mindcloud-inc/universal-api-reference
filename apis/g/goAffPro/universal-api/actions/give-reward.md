# GoAffPro: Give Reward

Creates a reward for an affiliate in GoAffPro.

```
POST https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/give-reward
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/give-reward" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rewards[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/give-reward', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rewards[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rewards[]` | array<object> | yes | Rewards to give to affiliates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": 1,
      "amount": 1,
      "id": 1,
      "metadata": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | number | Affiliate ID receiving the reward. |
| `amount` | number | Reward amount. |
| `id` | number | Created reward ID. |
| `metadata` | string | Reward metadata. |
| `status` | string | Reward status. |
| `type` | string | Reward type. |

## Native endpoint

Through the native GoAffPro API, this operation is `POST /admin/rewards` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/give-reward.md) for the provider-specific parameters and requirements.

