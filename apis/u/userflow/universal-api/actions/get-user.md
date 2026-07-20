# Userflow: Get User

Retrieves a user from Userflow by ID.

```
GET https://connect.mindcloud.co/v1/universal/userflow/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userflow/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes | The Userflow user ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "groups": {},
      "id": "string",
      "memberships": {},
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | User attributes. |
| `attributes.email` | string | User email. |
| `attributes.name` | string | User name. |
| `created_at` | date | User creation timestamp. |
| `groups` | object | User groups. |
| `id` | string | User ID. |
| `memberships` | object | User memberships. |
| `object` | string | Returned object type. |

## Native endpoint

Through the native Userflow API, this operation is `GET /users/:user_id` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

