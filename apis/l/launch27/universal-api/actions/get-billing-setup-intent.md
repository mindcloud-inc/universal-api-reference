# Launch27: Get Billing Setup Intent

Retrieves a billing setup intent from Launch27.

```
GET https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-billing-setup-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-billing-setup-intent?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-billing-setup-intent?${params}`, {
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
| `email` | string | yes | Customer email used to request a billing setup intent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "stripe_setup_intent_secret": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stripe_setup_intent_secret` | string | Stripe setup intent secret returned for client-side card setup. |

## Native endpoint

Through the native Launch27 API, this operation is `POST setup/billing/setup_intent` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billing-setup-intent.md) for the provider-specific parameters and requirements.

