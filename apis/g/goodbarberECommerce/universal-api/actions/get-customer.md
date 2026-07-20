# Goodbarber eCommerce: Get Customer



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-customer?${params}`, {
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
| `customerId` | number | yes | Unique ID of the customer. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthday": "string",
      "client_num": 1,
      "email": "ava@example.com",
      "first_name": "Ava",
      "internal_note": "string",
      "is_customer": true,
      "last_name": "Chen",
      "phone": "string",
      "shipping_addresses": [
        {}
      ],
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthday` | string | <div class="field_description">Customer birth date.</div> |
| `client_num` | number | <div class="field_description">Number associated to the customer.</div> |
| `email` | string | <div class="field_description">Email of the customer.</div> |
| `first_name` | string | <div class="field_description">Customer first name.</div> |
| `internal_note` | string | <div class="field_description">Notes about the customer.</div> |
| `is_customer` | boolean | <div class="field_description">This attribute's value is <code>true</code> when the user is a customer, and <code>false</code> when the user is a prospect.</div> |
| `last_name` | string | <div class="field_description">Customer last name.</div> |
| `phone` | string | <div class="field_description">Customer phone number.</div> |
| `shipping_addresses` | array<object> | <div class="field_description">List of the customer's shipping addresses</div> |
| `user_id` | number | <div class="field_description">ID of the user.</div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/customer/:webzine_id/customer/:customer_id/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

