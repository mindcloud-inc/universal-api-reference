# Maildrip: Update a user's subscription plan



```
PUT https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-a-user-s-subscription-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-a-user-s-subscription-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-a-user-s-subscription-plan', {
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
| `priceId` | string | no | The ID of the new price plan |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientSecret": "string",
      "message": "string",
      "subscriptionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientSecret` | string |  |
| `message` | string |  |
| `subscriptionId` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/payment/stripe/subscription/update` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-user-s-subscription-plan.md) for the provider-specific parameters and requirements.

