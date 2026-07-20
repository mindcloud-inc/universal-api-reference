# Braintree: Create Customer

Creates a new customer in Braintree.

```
POST https://connect.mindcloud.co/v1/universal/braintree/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Braintree `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/braintree/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/braintree/latest/actions/create-customer', {
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
| `firstName` | string | no | Customer first name. |
| `lastName` | string | no | Customer last name. |
| `email` | string | no | Customer email address. |
| `company` | string | no | Customer company name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "legacyId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `createdAt` | string | Customer creation timestamp. |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string | GraphQL ID of the created customer. |
| `lastName` | string |  |
| `legacyId` | string | Legacy Braintree customer ID. |

## Native endpoint

Through the native Braintree API, this operation is `POST /graphql` (base URL `https://payments.sandbox.braintree-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

