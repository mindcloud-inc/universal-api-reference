# Paystack: Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/paystack/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paystack/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerCode` | string | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `phone` | string | no |  |
| `metadata` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "customer_code": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "identified": true,
      "last_name": "Chen",
      "metadata": {},
      "phone": "string",
      "risk_action": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `customer_code` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `identified` | boolean |  |
| `last_name` | string |  |
| `metadata` | object |  |
| `phone` | string |  |
| `risk_action` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `PUT /customer/:customerCode` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

