# Ascora: Create Customer

Creates a new customer in Ascora.

```
POST https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-customer', {
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
| `companyName` | string | no |  |
| `contactFirstName` | string | no |  |
| `contactLastName` | string | no |  |
| `emailAddress` | string | no |  |
| `phoneNumber` | string | no |  |
| `mobileNumber` | string | no |  |
| `onHold` | boolean | no |  |
| `billingCustomerOnHold` | boolean | no |  |
| `streetLine1` | string | no |  |
| `streetLine2` | string | no |  |
| `streetSuburb` | string | no |  |
| `streetPostcode` | string | no |  |
| `streetState` | string | no |  |
| `streetCountry` | string | no |  |
| `customerType.name` | string | no |  |
| `leadSource.name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {
        "companyName": "Ava Chen",
        "contactFirstName": "Ava",
        "contactLastName": "Chen",
        "customerId": "string",
        "customerType": {
          "name": "Ava Chen"
        },
        "emailAddress": "ava@example.com",
        "leadSource": {
          "name": "Ava Chen"
        },
        "mobileNumber": "string",
        "phoneNumber": "string"
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
| `customer.companyName` | string | Customer company name. |
| `customer.contactFirstName` | string | Primary contact first name. |
| `customer.contactLastName` | string | Primary contact last name. |
| `customer.customerId` | string | ID of the created customer. |
| `customer.customerType.name` | string | Customer type name. |
| `customer.emailAddress` | string | Customer email address. |
| `customer.leadSource.name` | string | Lead source name. |
| `customer.mobileNumber` | string | Customer mobile number. |
| `customer.phoneNumber` | string | Customer phone number. |
| `success` | boolean | Whether Ascora created the customer. |

## Native endpoint

Through the native Ascora API, this operation is `POST /Customers/Customer` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

