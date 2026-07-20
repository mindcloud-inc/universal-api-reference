# Bonusly: Fulfill Custom Reward Redemptions

Fulfills custom reward redemptions in Bonusly.

```
PUT https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/fulfill-custom-reward-redemptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bonusly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/fulfill-custom-reward-redemptions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/fulfill-custom-reward-redemptions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idList` | string | no | Custom reward redemption IDs to fulfill. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fulfilledAt": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fulfilledAt` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bonusly API, this operation is `POST /custom_rewards_redemptions/fulfill` (base URL `https://bonus.ly/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fulfill-custom-reward-redemptions.md) for the provider-specific parameters and requirements.

