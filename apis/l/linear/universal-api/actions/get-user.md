# Linear: Get User

Retrieves a user from Linear.

```
GET https://connect.mindcloud.co/v1/universal/linear/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linear/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linear/latest/actions/get-user?${params}`, {
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
| `userId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user": {
        "active": true,
        "admin": true,
        "createdAt": "string",
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user.active` | boolean |  |
| `user.admin` | boolean |  |
| `user.createdAt` | string |  |
| `user.displayName` | string |  |
| `user.email` | string |  |
| `user.id` | string |  |
| `user.name` | string |  |
| `user.updatedAt` | string |  |

## Native endpoint

Through the native Linear API, this operation is `POST` (base URL `https://api.linear.app/graphql/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

