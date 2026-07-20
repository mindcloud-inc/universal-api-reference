# Escrow.com: Get Customer

Retrieves a customer from Escrow.com.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-customer?${params}`, {
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
| `customerId` | number | yes | Escrow.com customer ID. Use `me` through the separate Get Current Customer action. |

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

Through the native Escrow.com API, this operation is `GET /customer/:customer_id` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

