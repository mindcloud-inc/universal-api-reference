# Stripe: Create Billing Portal Session



```
POST https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-billing-portal-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-billing-portal-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": "cus_..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-billing-portal-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": "cus_..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | string | yes | Example: `cus_...`. |
| `returnUrl` | string | no | Example: `https://example.com/account`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `configuration` | string | no | Example: `bpc_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configuration": "string",
      "created": 1,
      "customer": "string",
      "id": "string",
      "locale": "string",
      "returnUrl": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | string |  |
| `created` | number |  |
| `customer` | string |  |
| `id` | string |  |
| `locale` | string |  |
| `returnUrl` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `POST billing_portal/sessions` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-billing-portal-session.md) for the provider-specific parameters and requirements.

