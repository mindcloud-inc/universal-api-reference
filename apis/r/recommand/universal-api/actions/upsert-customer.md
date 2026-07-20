# Recommand: Upsert Customer

Finds a customer in Recommand, or creates one if no match is found.

```
POST https://connect.mindcloud.co/v1/universal/recommand/latest/actions/upsert-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/upsert-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "string",
  "city": "string",
  "country": "string",
  "name": "Ava Chen",
  "postalcode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/upsert-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "string",
    "city": "string",
    "country": "string",
    "name": "Ava Chen",
    "postalcode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | yes | The street address of the customer |
| `city` | string | yes | The city of the customer |
| `country` | string | yes | The country code (ISO 3166-1 alpha-2) of the customer |
| `email` | string | no | The email address of the customer |
| `enterprisenumber` | string | no | The enterprise number of the customer |
| `externalid` | string | no | The external ID of the customer. If provided without id, finds by externalId and updates or creates if not found. |
| `id` | string | no | The internal ID of the customer to update. If provided, updates by id. |
| `name` | string | yes | The name of the customer |
| `peppoladdresses[]` | array<string> | no | The Peppol addresses of the customer |
| `phone` | string | no | The phone number of the customer |
| `postalcode` | string | yes | The postal code of the customer |
| `vatnumber` | string | no | The VAT number of the customer |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {
        "address": "string",
        "city": "string",
        "country": "string",
        "createdAt": "string",
        "email": "ava@example.com",
        "enterpriseNumber": "string",
        "externalId": "string",
        "id": "string",
        "name": "Ava Chen",
        "peppolAddresses": [
          "string"
        ],
        "phone": "string",
        "postalCode": "string",
        "teamId": "string",
        "updatedAt": "string",
        "vatNumber": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer` | object |  |
| `customer.address` | string |  |
| `customer.city` | string |  |
| `customer.country` | string |  |
| `customer.createdAt` | string |  |
| `customer.email` | string |  |
| `customer.enterpriseNumber` | string |  |
| `customer.externalId` | string |  |
| `customer.id` | string |  |
| `customer.name` | string |  |
| `customer.peppolAddresses` | array<string> |  |
| `customer.phone` | string |  |
| `customer.postalCode` | string |  |
| `customer.teamId` | string |  |
| `customer.updatedAt` | string |  |
| `customer.vatNumber` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `POST /api/v1/customers` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-customer.md) for the provider-specific parameters and requirements.

