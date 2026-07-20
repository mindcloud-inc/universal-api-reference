# GoAffPro: Update Reward

Updates an existing reward in GoAffPro.

```
PUT https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/update-reward
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/update-reward" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/update-reward', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Reward ID. |
| `status` | string | no | Reward status. |
| `amount` | number | no | Reward amount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Updated reward amount. |
| `success` | boolean | Whether the reward update succeeded. |

## Native endpoint

Through the native GoAffPro API, this operation is `PATCH /admin/rewards/:id` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reward.md) for the provider-specific parameters and requirements.

