# Vyte: Retrieve User

Retrieves a user from Vyte.

```
GET https://connect.mindcloud.co/v1/universal/vyte/latest/actions/retrieve-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vyte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/retrieve-user?connectionId=$CONNECTION_ID&userId=69ca9fead310017cb903a0fd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "69ca9fead310017cb903a0fd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vyte/latest/actions/retrieve-user?${params}`, {
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
| `userId` | string | yes | The Vyte user ID. Default: `69ca9fead310017cb903a0fd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "emails": [
        "ava@example.com"
      ],
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "last_name": "Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `emails` | array<string> |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `last_name` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Vyte API, this operation is `GET v2/users/:user_id` (base URL `https://api.vyte.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-user.md) for the provider-specific parameters and requirements.

