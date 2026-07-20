# GoCardless: Create Customer

Creates a new customer in GoCardless.

```
POST https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no |  |
| `givenName` | string | no |  |
| `familyName` | string | no |  |
| `companyName` | string | no |  |
| `addressLine1` | string | no |  |
| `addressLine2` | string | no |  |
| `addressLine3` | string | no |  |
| `city` | string | no |  |
| `postalCode` | string | no |  |
| `countryCode` | string | no |  |
| `region` | string | no |  |
| `language` | list | no | One of: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNumber` | string | no |  |
| `danishIdentityNumber` | string | no |  |
| `swedishIdentityNumber` | string | no |  |
| `metadata` | object | no |  |

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

Through the native GoCardless API, this operation is `POST /customers` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

