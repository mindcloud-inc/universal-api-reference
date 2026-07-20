# Yotpo Loyalty & Referrals: Fetch VIP Tiers

Retrieves VIP tiers from Yotpo Loyalty & Referrals.

```
GET https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/fetch-vip-tiers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/fetch-vip-tiers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/fetch-vip-tiers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "couponReward": "string",
      "description": "string",
      "entryThreshold": {},
      "id": 1,
      "name": "Ava Chen",
      "pointsMultiplier": "string",
      "pointsReward": 1,
      "regainThreshold": {},
      "retainThreshold": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `couponReward` | string | Coupon reward associated with the tier when configured. |
| `description` | string | VIP tier description shown in Yotpo. |
| `entryThreshold` | object | Thresholds required to enter the tier. |
| `id` | number | VIP tier identifier. |
| `name` | string | VIP tier name. |
| `pointsMultiplier` | string | Points multiplier applied to the tier. |
| `pointsReward` | number | Points reward granted for entering the tier. |
| `regainThreshold` | object | Thresholds required to regain the tier after losing it. |
| `retainThreshold` | object | Thresholds required to retain the tier. |
| `type` | string | VIP tier type returned by Yotpo. |

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `GET /api/v2/vip_tiers` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-vip-tiers.md) for the provider-specific parameters and requirements.

