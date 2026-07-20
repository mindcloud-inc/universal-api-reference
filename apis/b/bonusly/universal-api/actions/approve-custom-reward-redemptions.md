# Bonusly: Approve Custom Reward Redemptions

Approves custom reward redemptions in Bonusly.

```
PUT https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/approve-custom-reward-redemptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bonusly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/approve-custom-reward-redemptions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idList": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/approve-custom-reward-redemptions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idList": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idList` | string | yes | Custom reward redemption IDs to approve. |
| `state` | string | no | Optional approval state value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvedAt": "string",
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
| `approvedAt` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bonusly API, this operation is `POST /custom_rewards_redemptions/approve` (base URL `https://bonus.ly/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-custom-reward-redemptions.md) for the provider-specific parameters and requirements.

