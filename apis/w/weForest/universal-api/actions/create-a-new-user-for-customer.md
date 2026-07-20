# WeForest: Create a new user for customer

Creates a new customer user in WeForest.

```
POST https://connect.mindcloud.co/v1/universal/weForest/latest/actions/create-a-new-user-for-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeForest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/create-a-new-user-for-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weForest/latest/actions/create-a-new-user-for-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Customer identifier from WeForest. |
| `firstName` | string | yes | First name for the new customer user. |
| `lastName` | string | yes | Last name for the new customer user. |
| `email` | string | yes | Email for the new customer user. |
| `password` | string | yes | Password for the new customer user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activationToken": "string",
      "active": true,
      "customerId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activationToken` | string |  |
| `active` | boolean |  |
| `customerId` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `role` | string |  |

## Native endpoint

Through the native WeForest API, this operation is `POST /customers/:id/users` (base URL `https://api.weforest.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-user-for-customer.md) for the provider-specific parameters and requirements.

