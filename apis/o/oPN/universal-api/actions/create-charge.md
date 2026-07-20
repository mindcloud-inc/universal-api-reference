# OPN: Create Charge

Creates a new charge in OPN.

```
POST https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-charge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | The charge amount in the smallest currency unit. |
| `capture` | boolean | no | Whether to capture the charge immediately. |
| `currency` | string | yes | The three-letter currency code. |
| `customer` | string | no | The customer ID to charge. |
| `description` | string | no | The charge description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "authorized": true,
      "capture": true,
      "card": {},
      "created_at": "string",
      "currency": "string",
      "customer": "string",
      "description": "string",
      "failure_code": "string",
      "failure_message": "string",
      "id": "string",
      "link": "https://example.com",
      "livemode": true,
      "location": "string",
      "metadata": {},
      "object": "string",
      "paid": true,
      "paid_at": "string",
      "refunds": {},
      "source": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `authorized` | boolean |  |
| `capture` | boolean |  |
| `card` | object |  |
| `created_at` | string |  |
| `currency` | string |  |
| `customer` | string |  |
| `description` | string |  |
| `failure_code` | string |  |
| `failure_message` | string |  |
| `id` | string |  |
| `link` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `paid` | boolean |  |
| `paid_at` | string |  |
| `refunds` | object |  |
| `source` | object |  |
| `status` | string |  |

## Native endpoint

Through the native OPN API, this operation is `POST /charges` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-charge.md) for the provider-specific parameters and requirements.

