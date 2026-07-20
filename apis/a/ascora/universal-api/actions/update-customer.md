# Ascora: Update Customer

Updates an existing customer in Ascora.

```
PUT https://connect.mindcloud.co/v1/universal/ascora/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/update-customer', {
  method: 'PUT',
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
| `customerId` | string | no | Existing Ascora customer ID to update. |
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
| `customerType.name` | string | no | Ascora customer type name. |
| `leadSource.name` | string | no | Ascora lead source name. |

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
| `customer.companyName` | string | Customer company name after update. |
| `customer.contactFirstName` | string | Primary contact first name. |
| `customer.contactLastName` | string | Primary contact last name. |
| `customer.customerId` | string | Ascora customer ID. |
| `customer.customerType.name` | string | Customer type name. |
| `customer.emailAddress` | string | Customer email address. |
| `customer.leadSource.name` | string | Lead source name. |
| `customer.mobileNumber` | string | Customer mobile number. |
| `customer.phoneNumber` | string | Updated customer phone number. |
| `success` | boolean | Whether Ascora updated the customer. |

## Native endpoint

Through the native Ascora API, this operation is `POST /Customers/Customer` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

