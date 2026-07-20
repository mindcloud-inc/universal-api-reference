# Systeme.io: Cancel Subscription

Cancels an existing subscription in Systeme.io.

```
PUT https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/cancel-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/cancel-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "cancel": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/cancel-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "cancel": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Subscription identifier. |
| `cancel` | string | yes | Cancellation timing: Now or WhenBillingPeriodEnds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Systeme.io API, this operation is `POST /api/payment/subscriptions/:id/cancel` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-subscription.md) for the provider-specific parameters and requirements.

