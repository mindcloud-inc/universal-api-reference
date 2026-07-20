# Ascora: Get Customer

Retrieves a customer from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-customer?${params}`, {
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
| `id` | string | no | Ascora customer ID. |

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
| `customer.customerId` | string | Ascora customer ID. |
| `customer.customerType.name` | string | Customer type name. |
| `customer.emailAddress` | string | Customer email address. |
| `customer.leadSource.name` | string | Lead source name. |
| `customer.mobileNumber` | string | Customer mobile number. |
| `customer.phoneNumber` | string | Customer phone number. |
| `success` | boolean | Whether Ascora returned the customer. |

## Native endpoint

Through the native Ascora API, this operation is `GET /Customers/Customer/{{id}}` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

