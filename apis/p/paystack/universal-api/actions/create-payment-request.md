# Paystack: Create Payment Request



```
POST https://connect.mindcloud.co/v1/universal/paystack/latest/actions/create-payment-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/create-payment-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": "string",
  "amount": 1,
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paystack/latest/actions/create-payment-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": "string",
    "amount": 1,
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | string | yes |  |
| `amount` | number | yes |  |
| `description` | string | yes |  |
| `dueDate` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdAt": "string",
      "currency": "string",
      "customer": {},
      "description": "string",
      "due_date": "string",
      "id": 1,
      "invoice_number": 1,
      "offline_reference": "string",
      "paid": true,
      "request_code": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customer` | object |  |
| `description` | string |  |
| `due_date` | string |  |
| `id` | number |  |
| `invoice_number` | number |  |
| `offline_reference` | string |  |
| `paid` | boolean |  |
| `request_code` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `POST /paymentrequest` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-request.md) for the provider-specific parameters and requirements.

