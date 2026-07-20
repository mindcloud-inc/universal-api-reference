# Recommand: Get Customer

Retrieves a customer record from Recommand.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-customer?${params}`, {
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
| `customerid` | string | yes | customerId parameter. |

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

Through the native Recommand API, this operation is `GET /api/v1/customers/:customerId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

