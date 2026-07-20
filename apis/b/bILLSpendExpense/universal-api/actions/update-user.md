# BILL Spend & Expense: Update User

Updates an existing user in BILL Spend & Expense.

```
PUT https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateOfBirth` | date | no | User date of birth in yyyy-MM-dd format. |
| `email` | string | no | User email address. |
| `firstName` | string | no | User first name. |
| `lastName` | string | no | User last name. |
| `role` | string | no | User role. |
| `userId` | list | yes | BILL-generated ID or UUID of the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasDateOfBirth": true,
      "id": "string",
      "lastName": "Chen",
      "retired": true,
      "role": "string",
      "smsOptIn": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `hasDateOfBirth` | boolean |  |
| `id` | string |  |
| `lastName` | string |  |
| `retired` | boolean |  |
| `role` | string |  |
| `smsOptIn` | boolean |  |
| `uuid` | string |  |

## Native endpoint

Through the native BILL Spend & Expense API, this operation is `PATCH spend/users/:userId` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

