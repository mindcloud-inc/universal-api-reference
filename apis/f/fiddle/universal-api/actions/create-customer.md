# Fiddle: Create Customer

Creates a new customer in Fiddle.

```
POST https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Customer name |
| `email` | string | no | Customer email |
| `phone` | string | no | Customer phone |
| `address` | string | no | Customer address line 1 |
| `address2` | string | no | Customer address line 2 |
| `city` | string | no | Customer city |
| `state` | string | no | Customer state |
| `zip` | string | no | Customer ZIP or postal code |
| `country` | string | no | Customer country |
| `fax` | string | no | Customer fax |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingAddressInput` | object | no | Billing address object |
| `shippingAddressInput` | object | no | Shipping address object |
| `contacts[]` | array<object> | no | Array of customer contacts |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer` | object |  |
| `customer.createdAt` | date |  |
| `customer.id` | string |  |
| `customer.name` | string |  |
| `customer.updatedAt` | date |  |

## Native endpoint

Through the native Fiddle API, this operation is `POST /customers` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

