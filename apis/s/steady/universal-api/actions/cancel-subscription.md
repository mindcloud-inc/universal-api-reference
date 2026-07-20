# Steady: Cancel Subscription

Cancels a Steady subscription at the current term's end.

```
PUT https://connect.mindcloud.co/v1/universal/steady/latest/actions/cancel-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Steady `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/steady/latest/actions/cancel-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/steady/latest/actions/cancel-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionId` | string | yes | The Steady subscription ID to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "currency": "string",
          "period": "string",
          "state": "string"
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.currency` | string |  |
| `data.attributes.period` | string |  |
| `data.attributes.state` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native Steady API, this operation is `POST /subscriptions/:subscription_id/cancel` (base URL `https://steadyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-subscription.md) for the provider-specific parameters and requirements.

