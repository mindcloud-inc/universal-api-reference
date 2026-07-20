# Launch27: Authorize Billing Charge

Authorizes a billing charge in Launch27.

```
PUT https://connect.mindcloud.co/v1/universal/launch27/latest/actions/authorize-billing-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/authorize-billing-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "token": "string",
  "stripe_setup_intent_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launch27/latest/actions/authorize-billing-charge', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "token": "string",
    "stripe_setup_intent_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `token` | string | yes | Billing token to authorize. |
| `stripe_setup_intent_id` | string | yes | Stripe setup intent ID to pair with the authorization call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "stripe_payment_intent_secret": "string",
      "stripe_requires_action": true,
      "stripe_setup_intent_secret": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stripe_payment_intent_secret` | string | Stripe payment intent secret used when additional action is required. |
| `stripe_requires_action` | boolean | Whether the Stripe flow requires an additional customer action step. |
| `stripe_setup_intent_secret` | string | Stripe setup intent secret returned when a new card setup is required. |

## Native endpoint

Through the native Launch27 API, this operation is `POST setup/billing/authorize_charge` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authorize-billing-charge.md) for the provider-specific parameters and requirements.

