# ChargeDesk: Update Customer

Updates an existing customer in ChargeDesk.

```
PUT https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | Customer ID to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card_on_file": "string",
      "charges": 1,
      "company": "string",
      "country": "string",
      "customer_id": "string",
      "description": "string",
      "email": "ava@example.com",
      "first_seen": 1,
      "gateway_url": "https://example.com",
      "manage_url": "https://example.com",
      "methods_active": [
        "string"
      ],
      "methods_supported": [
        "string"
      ],
      "name": "Ava Chen",
      "object": "string",
      "phone": "string",
      "username": "Ava Chen",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card_on_file` | string |  |
| `charges` | number |  |
| `company` | string |  |
| `country` | string |  |
| `customer_id` | string |  |
| `description` | string |  |
| `email` | string |  |
| `first_seen` | number |  |
| `gateway_url` | string |  |
| `manage_url` | string |  |
| `methods_active` | array<string> |  |
| `methods_supported` | array<string> |  |
| `name` | string |  |
| `object` | string |  |
| `phone` | string |  |
| `username` | string |  |
| `website` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `POST /customers/:CUSTOMER_ID` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

