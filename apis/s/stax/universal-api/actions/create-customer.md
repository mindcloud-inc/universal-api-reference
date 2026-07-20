# Stax: Create Customer

Creates a customer in Stax.

```
POST https://connect.mindcloud.co/v1/universal/stax/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stax/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stax/latest/actions/create-customer', {
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
| `email` | string | no | Customer email |
| `firstname` | string | no | Customer first name |
| `lastname` | string | no | Customer last name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "address2": "string",
      "addressCity": "string",
      "addressCountry": "string",
      "addressState": "string",
      "addressZip": "string",
      "allowInvoiceCreditCardPayments": true,
      "company": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "hasAddress": true,
      "id": "string",
      "lastname": "Chen",
      "missingAddressComponents": [
        "string"
      ],
      "phone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string | Primary street address. |
| `address2` | string | Secondary street address. |
| `addressCity` | string | City. |
| `addressCountry` | string | Country. |
| `addressState` | string | State or region. |
| `addressZip` | string | Postal code. |
| `allowInvoiceCreditCardPayments` | boolean | Whether invoices may be paid by card. |
| `company` | string | Customer company name. |
| `createdAt` | string | Creation timestamp. |
| `email` | string | Customer email address. |
| `firstname` | string | Customer first name. |
| `hasAddress` | boolean | Whether the customer record has a complete address. |
| `id` | string | Stax customer identifier. |
| `lastname` | string | Customer last name. |
| `missingAddressComponents` | array<string> | Missing address fields reported by Stax. |
| `phone` | string | Customer phone number. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Stax API, this operation is `POST /customer` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

