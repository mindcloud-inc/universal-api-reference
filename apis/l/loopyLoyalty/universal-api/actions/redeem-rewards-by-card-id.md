# Loopy Loyalty: Redeem Rewards By Card ID



```
PUT https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/redeem-rewards-by-card-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/redeem-rewards-by-card-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cid": "RDX5AsgKYa3UZ7",
  "rewardType": "1",
  "rewardsToRedeem": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/redeem-rewards-by-card-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cid": "RDX5AsgKYa3UZ7",
    "rewardType": "1",
    "rewardsToRedeem": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cid` | string | yes | Example: `RDX5AsgKYa3UZ7`. |
| `rewardType` | number | yes | Example: `1`. |
| `rewardsToRedeem` | number | yes | Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scanLatitude` | number | no | Example: `37.7749`. |
| `scanLongitude` | number | no | Example: `-122.4194`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the rewards were redeemed successfully. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /card/cid/:cid/redeemReward/:rewardType/:rewardsToRedeem` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/redeem-rewards-by-card-id.md) for the provider-specific parameters and requirements.

