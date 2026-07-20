# Escrow.com: Create Customer

Creates a new customer in Escrow.com.

```
POST https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Customer email address. |
| `firstName` | string | yes | Customer first name. |
| `lastName` | string | yes | Customer last name. |
| `phoneNumber` | string | no | Customer phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountType": "string",
      "address": {},
      "company": {},
      "customerEmailVerification": {},
      "displayName": "Ava Chen",
      "electronicVerification": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "phoneNumber": "string",
      "verification": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string | Escrow.com account type. |
| `address` | object | Customer address details. |
| `company` | object | Company profile details. |
| `customerEmailVerification` | object | Email verification status. |
| `displayName` | string | Customer display name. |
| `electronicVerification` | object | Electronic verification details. |
| `email` | string | Customer email address. |
| `firstName` | string | Customer first name. |
| `id` | number | Escrow.com customer ID. |
| `lastName` | string | Customer last name. |
| `phoneNumber` | string | Customer phone number. |
| `verification` | object | Customer verification status. |

## Native endpoint

Through the native Escrow.com API, this operation is `POST /customer` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

