# Braintree: Update Customer

Updates an existing customer in Braintree.

```
PUT https://connect.mindcloud.co/v1/universal/braintree/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Braintree `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/braintree/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/braintree/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | The GraphQL ID of the customer to update. |
| `company` | string | no | Updated company value for the customer. |

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
| `id` | string | GraphQL ID of the updated customer. |
| `lastName` | string |  |
| `legacyId` | string | Legacy Braintree customer ID. |

## Native endpoint

Through the native Braintree API, this operation is `POST /graphql` (base URL `https://payments.sandbox.braintree-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

