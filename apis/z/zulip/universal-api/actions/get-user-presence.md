# Zulip: Get User Presence

Retrieves a Zulip user's presence information.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-user-presence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-user-presence?connectionId=$CONNECTION_ID&userIdOrEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userIdOrEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-user-presence?${params}`, {
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
| `userIdOrEmail` | string | yes | The target user's ID or email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "presence": {},
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string |  |
| `presence` | object |  |
| `result` | string |  |

## Native endpoint

Through the native Zulip API, this operation is `GET /users/:user_id_or_email/presence` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-presence.md) for the provider-specific parameters and requirements.

