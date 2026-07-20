# Blue: Get User

Retrieves a user from Blue by ID.

```
GET https://connect.mindcloud.co/v1/universal/blue/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blue/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blue/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes | Blue user node ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string",
      "role": "string",
      "uid": "string",
      "workspaceCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `role` | string |  |
| `uid` | string |  |
| `workspaceCount` | number |  |

## Native endpoint

Through the native Blue API, this operation is `POST /graphql` (base URL `https://api.blue.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

