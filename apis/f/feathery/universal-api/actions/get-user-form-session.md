# Feathery: Get User Form Session



```
GET https://connect.mindcloud.co/v1/universal/feathery/latest/actions/get-user-form-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/get-user-form-session?connectionId=$CONNECTION_ID&user_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/get-user-form-session?${params}`, {
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
| `user_id` | string | yes | The user ID whose form session you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auth_id": "string",
      "forms": [
        {}
      ],
      "internal_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth_id` | string | The identity provider ID when present. |
| `forms` | array<object> | The forms the user is working on. |
| `internal_id` | string | The unique user ID. |

## Native endpoint

Through the native Feathery API, this operation is `GET /api/user/:user_id/session/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-form-session.md) for the provider-specific parameters and requirements.

