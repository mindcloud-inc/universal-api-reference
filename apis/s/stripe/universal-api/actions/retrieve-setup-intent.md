# Stripe: Retrieve SetupIntent



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-setup-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-setup-intent?connectionId=$CONNECTION_ID&setupIntent=seti_..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "setupIntent": "seti_..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-setup-intent?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `setupIntent` | string | yes | Stripe SetupIntent ID returned by the completed setup-mode Checkout Session, for example seti_... Example: `seti_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "customer": "string",
      "description": "string",
      "id": "string",
      "latestAttempt": "string",
      "livemode": true,
      "object": "string",
      "paymentMethod": "string",
      "paymentMethodTypes": [
        "string"
      ],
      "status": "string",
      "usage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Creation timestamp in seconds |
| `customer` | string | Stripe Customer ID associated with the SetupIntent |
| `description` | string | SetupIntent description |
| `id` | string | Stripe SetupIntent ID |
| `latestAttempt` | string | Latest SetupAttempt ID when available |
| `livemode` | boolean | Whether the SetupIntent exists in live mode |
| `object` | string | Stripe object type |
| `paymentMethod` | string | PaymentMethod ID created or selected by the completed SetupIntent |
| `paymentMethodTypes` | array<string> | Payment method types allowed for the SetupIntent |
| `status` | string | SetupIntent status |
| `usage` | string | Expected future usage, such as off_session |

## Native endpoint

Through the native Stripe API, this operation is `GET setup_intents/:setupIntent` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-setup-intent.md) for the provider-specific parameters and requirements.

