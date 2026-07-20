# Zulip: Get User by Email

Retrieves a specific Zulip user by email address.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-user-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-user-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-user-by-email?${params}`, {
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
| `email` | string | yes | The target user's Zulip API email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "result": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string |  |
| `result` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Zulip API, this operation is `GET /users/:email` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-by-email.md) for the provider-specific parameters and requirements.

