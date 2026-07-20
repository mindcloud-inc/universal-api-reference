# BILL Spend & Expense: Get User

Retrieves a user from BILL Spend & Expense.

```
GET https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/get-user?${params}`, {
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
      "phoneNumber": "string",
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
| `phoneNumber` | string |  |
| `retired` | boolean |  |
| `role` | string |  |
| `smsOptIn` | boolean |  |
| `uuid` | string |  |

## Native endpoint

Through the native BILL Spend & Expense API, this operation is `GET spend/users/:userId` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

