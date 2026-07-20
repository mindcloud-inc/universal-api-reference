# Reward Sciences: Bid On Reward



```
POST https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/bid-on-reward
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reward Sciences `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/bid-on-reward" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rewardId": 1,
  "userId": 1,
  "amount": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/bid-on-reward', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rewardId": 1,
    "userId": 1,
    "amount": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rewardId` | number | yes | The Reward Sciences reward ID. |
| `userId` | number | yes | The user placing the bid. |
| `amount` | string | yes | Bid amount or the literal value max. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Bid record ID when returned. |
| `user_id` | number | User ID associated with the bid when returned. |

## Native endpoint

Through the native Reward Sciences API, this operation is `POST /rewards/:rewardId/bids` (base URL `https://api.rewardsciences.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bid-on-reward.md) for the provider-specific parameters and requirements.

