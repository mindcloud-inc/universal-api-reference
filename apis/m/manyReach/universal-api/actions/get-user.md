# ManyReach: Get User

Retrieves a user from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-user?${params}`, {
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
| `id` | string | no | User ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailConfirmed": true,
      "firstName": "Ava",
      "lastName": "Chen",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `emailConfirmed` | boolean |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/users/:id` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

