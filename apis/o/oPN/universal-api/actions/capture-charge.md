# OPN: Capture Charge

Captures an existing charge in OPN.

```
PUT https://connect.mindcloud.co/v1/universal/oPN/latest/actions/capture-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/capture-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/capture-charge', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `capture_amount` | number | no | A partial amount to capture. |
| `id` | string | yes | The charge ID to capture. |

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

Through the native OPN API, this operation is `POST /charges/:id/capture` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capture-charge.md) for the provider-specific parameters and requirements.

