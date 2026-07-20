# Deepset: Get User

Retrieves a Deepset user by ID.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes | deepset user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "email": "ava@example.com",
      "family_name": "Ava Chen",
      "given_name": "Ava Chen",
      "oauth_provider": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `email` | string |  |
| `family_name` | string |  |
| `given_name` | string |  |
| `oauth_provider` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v1/users/:user_id` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

