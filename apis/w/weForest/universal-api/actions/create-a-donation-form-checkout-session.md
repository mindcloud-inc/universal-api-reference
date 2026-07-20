# WeForest: Create a donation form checkout session

Creates a donation form checkout session in WeForest.

```
POST https://connect.mindcloud.co/v1/universal/weForest/latest/actions/create-a-donation-form-checkout-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeForest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/create-a-donation-form-checkout-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "items[]": [
    {}
  ],
  "user": {},
  "successUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weForest/latest/actions/create-a-donation-form-checkout-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "items[]": [{}],
    "user": {},
    "successUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Donation form identifier from WeForest. |
| `items[]` | array<object> | yes | Array of donation items with productId and quantity. |
| `user` | object | yes | Donor user object with email and name. |
| `successUrl` | string | yes | URL to redirect to after successful checkout. |
| `cancelUrl` | string | no | URL to redirect to if checkout is cancelled. |
| `currency` | string | no | Checkout currency code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkoutUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkoutUrl` | string |  |

## Native endpoint

Through the native WeForest API, this operation is `POST /forms/:id/checkout` (base URL `https://api.weforest.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-donation-form-checkout-session.md) for the provider-specific parameters and requirements.

