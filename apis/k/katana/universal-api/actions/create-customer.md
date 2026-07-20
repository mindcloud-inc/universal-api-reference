# Katana: Create Customer

Creates a new customer in Katana.

```
POST https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-customer', {
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
| `name` | string | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `company` | string | no |  |
| `email` | string | no |  |
| `phone` | string | no |  |
| `currency` | string | no | The customer’s currency (ISO 4217). |
| `referenceId` | string | no |  |
| `category` | string | no |  |
| `comment` | string | no |  |
| `discountRate` | number | no |  |
| `addresses[]` | array<object> | no |  |
| `addresses[].entityType` | string | no |  |
| `addresses[].default` | boolean | no |  |
| `addresses[].firstName` | string | no |  |
| `addresses[].lastName` | string | no |  |
| `addresses[].company` | string | no |  |
| `addresses[].phone` | string | no |  |
| `addresses[].line1` | string | no |  |
| `addresses[].line2` | string | no |  |
| `addresses[].city` | string | no |  |
| `addresses[].state` | string | no |  |
| `addresses[].zip` | string | no |  |
| `addresses[].country` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {
          "city": "string",
          "company": "string",
          "country": "string",
          "createdAt": "string",
          "customerId": 1,
          "entityType": "string",
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "line1": "string",
          "line2": "string",
          "phone": "string",
          "state": "string",
          "updatedAt": "string",
          "zip": "string"
        }
      ],
      "category": "string",
      "comment": "string",
      "company": "string",
      "createdAt": "string",
      "currency": "string",
      "defaultBillingId": 1,
      "defaultShippingId": 1,
      "deletedAt": "string",
      "discountRate": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "phone": "string",
      "referenceId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `addresses[].city` | string |  |
| `addresses[].company` | string |  |
| `addresses[].country` | string |  |
| `addresses[].createdAt` | string |  |
| `addresses[].customerId` | number |  |
| `addresses[].entityType` | string |  |
| `addresses[].firstName` | string |  |
| `addresses[].id` | number |  |
| `addresses[].lastName` | string |  |
| `addresses[].line1` | string |  |
| `addresses[].line2` | string |  |
| `addresses[].phone` | string |  |
| `addresses[].state` | string |  |
| `addresses[].updatedAt` | string |  |
| `addresses[].zip` | string |  |
| `category` | string |  |
| `comment` | string |  |
| `company` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `defaultBillingId` | number |  |
| `defaultShippingId` | number |  |
| `deletedAt` | string |  |
| `discountRate` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `referenceId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `POST /customers` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

