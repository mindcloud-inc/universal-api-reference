# Poof: Create Checkout

Creates a new checkout in Poof.

```
POST https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-checkout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-checkout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "Poof",
  "amount": "2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-checkout', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "Poof",
    "amount": "2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | Checkout username from the Poof docs example. Default: `Poof`. |
| `amount` | string | yes | Checkout amount. Default: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Poof API, this operation is `POST https://www.poof.io/api/v1/checkout` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checkout.md) for the provider-specific parameters and requirements.

