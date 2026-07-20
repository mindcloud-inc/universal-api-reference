# Loopy Loyalty: Redeem Rewards By Unique Card Data Field



```
PUT https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/redeem-rewards-by-unique-card-data-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/redeem-rewards-by-unique-card-data-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "5fcDywPejwj9QszwngBTKg",
  "uniqueIdType": "email",
  "uniqueIdValue": "taylor.stage3.1774385507840@example.com",
  "rewardType": "1",
  "rewardsToRedeem": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/redeem-rewards-by-unique-card-data-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "5fcDywPejwj9QszwngBTKg",
    "uniqueIdType": "email",
    "uniqueIdValue": "taylor.stage3.1774385507840@example.com",
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
| `campaignId` | string | yes | Example: `5fcDywPejwj9QszwngBTKg`. |
| `uniqueIdType` | string | yes | Example: `email`. |
| `uniqueIdValue` | string | yes | Example: `taylor.stage3.1774385507840@example.com`. |
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

Through the native Loopy Loyalty API, this operation is `POST /uniquecard/campaignid/:campaignId/:uniqueIdType/:uniqueIdValue/redeemReward/:rewardType/:rewardsToRedeem` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/redeem-rewards-by-unique-card-data-field.md) for the provider-specific parameters and requirements.

