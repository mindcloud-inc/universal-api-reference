# Mailchimp: Update Customer

Updates an existing customer in a Mailchimp e-commerce store.

```
PUT https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "store_id": "string",
  "customer_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "store_id": "string",
    "customer_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | object | no |  |
| `address.address1` | string | no |  |
| `address.address2` | string | no |  |
| `address.city` | string | no |  |
| `address.country` | string | no |  |
| `address.country_code` | string | no |  |
| `address.postal_code` | string | no |  |
| `address.province` | string | no |  |
| `address.province_code` | string | no |  |
| `company` | string | no |  |
| `store_id` | string | yes | The store id. |
| `customer_id` | string | yes | The customer id. |
| `opt_in_status` | boolean | no | Whether the customer has opted in to email marketing. |
| `first_name` | string | no | Customer first name. |
| `last_name` | string | no | Customer last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "links": {},
      "optInStatus": true,
      "ordersCount": 1,
      "totalSpent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Customer address. |
| `emailAddress` | string | The customer's email address. |
| `firstName` | string | Customer first name. |
| `id` | string | The customer's unique ID. |
| `lastName` | string | Customer last name. |
| `links` | object | Link relations. |
| `optInStatus` | boolean | Whether the customer is opted in. |
| `ordersCount` | number | Number of orders for this customer. |
| `totalSpent` | number | Total amount spent by the customer. |

## Native endpoint

Through the native Mailchimp API, this operation is `PATCH ecommerce/stores/:store_id/customers/:customer_id` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

