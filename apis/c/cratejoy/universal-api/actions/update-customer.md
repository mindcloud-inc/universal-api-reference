# Cratejoy: Update Customer

Updates an existing customer in Cratejoy.

```
PUT https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | The Cratejoy customer ID. |
| `firstName` | string | no | The customer's first name. |
| `lastName` | string | no | The customer's last name. |
| `email` | string | no | The customer's email address. |
| `note` | string | no | A note to prepend to the customer's existing note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "name": "Ava Chen",
      "num_orders": 1,
      "num_subscriptions": 1,
      "subscription_status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `last_name` | string |  |
| `name` | string |  |
| `num_orders` | number |  |
| `num_subscriptions` | number |  |
| `subscription_status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Cratejoy API, this operation is `PUT /v1/customers/:customerId/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

