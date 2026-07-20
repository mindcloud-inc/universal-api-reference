# Mailchimp: Add Customer

Creates a new customer in a Mailchimp e-commerce store.

```
POST https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "store_id": "string",
  "id": "string",
  "email_address": "ava@example.com",
  "opt_in_status": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "store_id": "string",
    "id": "string",
    "email_address": "ava@example.com",
    "opt_in_status": true
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
| `first_name` | string | no |  |
| `last_name` | string | no |  |
| `sms_phone_number` | string | no |  |
| `store_id` | string | yes | The store id. |
| `id` | string | yes | A unique identifier for the customer in your system. |
| `email_address` | string | yes | The customer's email address. |
| `opt_in_status` | boolean | yes | Whether the customer has opted in to email marketing. |

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
      "optInStatus": true
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

## Native endpoint

Through the native Mailchimp API, this operation is `POST ecommerce/stores/:store_id/customers` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-customer.md) for the provider-specific parameters and requirements.

