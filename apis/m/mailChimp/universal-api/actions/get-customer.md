# Mailchimp: Get Customer

Retrieves a customer from a Mailchimp e-commerce store.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-customer?connectionId=$CONNECTION_ID&store_id=string&customer_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "store_id": "string",
  "customer_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-customer?${params}`, {
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
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `store_id` | string | yes | The store id. |
| `customer_id` | string | yes | The customer id. |

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

Through the native Mailchimp API, this operation is `GET ecommerce/stores/:store_id/customers/:customer_id` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

