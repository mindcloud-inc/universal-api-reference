# GoCardless: Get Customer

Retrieves a single customer from GoCardless.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-customer?${params}`, {
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
| `customerId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": {
        "addressLine1": {},
        "addressLine2": {},
        "addressLine3": {},
        "city": {},
        "companyName": {},
        "countryCode": "string",
        "createdAt": "string",
        "danishIdentityNumber": {},
        "email": "ava@example.com",
        "familyName": "Ava Chen",
        "givenName": "Ava Chen",
        "id": "string",
        "language": "string",
        "phoneNumber": {},
        "postalCode": {},
        "region": {},
        "swedishIdentityNumber": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers.addressLine1` | object |  |
| `customers.addressLine2` | object |  |
| `customers.addressLine3` | object |  |
| `customers.city` | object |  |
| `customers.companyName` | object |  |
| `customers.countryCode` | string |  |
| `customers.createdAt` | string |  |
| `customers.danishIdentityNumber` | object |  |
| `customers.email` | string |  |
| `customers.familyName` | string |  |
| `customers.givenName` | string |  |
| `customers.id` | string |  |
| `customers.language` | string |  |
| `customers.phoneNumber` | object |  |
| `customers.postalCode` | object |  |
| `customers.region` | object |  |
| `customers.swedishIdentityNumber` | object |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /customers/:customerId` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

