# OPN: Create Link

Creates a new link in OPN.

```
POST https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "currency": "string",
  "description": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "currency": "string",
    "description": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | The amount to collect, in the smallest currency unit. |
| `currency` | string | yes | The three-letter currency code. |
| `description` | string | yes | The payment link description. |
| `multiple` | boolean | no | Whether the payment link can be used multiple times. |
| `title` | string | yes | The payment link title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "charges": {},
      "created_at": "string",
      "currency": "string",
      "deleted": true,
      "deleted_at": "string",
      "description": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "merchant_name": "Ava Chen",
      "merchant_uid": "string",
      "multiple": true,
      "object": "string",
      "payment_uri": "string",
      "title": "string",
      "used": true,
      "used_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `charges` | object |  |
| `created_at` | string |  |
| `currency` | string |  |
| `deleted` | boolean |  |
| `deleted_at` | string |  |
| `description` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `merchant_name` | string |  |
| `merchant_uid` | string |  |
| `multiple` | boolean |  |
| `object` | string |  |
| `payment_uri` | string |  |
| `title` | string |  |
| `used` | boolean |  |
| `used_at` | string |  |

## Native endpoint

Through the native OPN API, this operation is `POST /links` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-link.md) for the provider-specific parameters and requirements.

