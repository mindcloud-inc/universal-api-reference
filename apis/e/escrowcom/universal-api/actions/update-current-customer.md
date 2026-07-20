# Escrow.com: Update Current Customer

Updates the current customer in Escrow.com.

```
PUT https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/update-current-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/update-current-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/update-current-customer', {
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
| `firstName` | string | no | Customer first name. |
| `lastName` | string | no | Customer last name. |
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

Through the native Escrow.com API, this operation is `PATCH /customer/me` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-current-customer.md) for the provider-specific parameters and requirements.

