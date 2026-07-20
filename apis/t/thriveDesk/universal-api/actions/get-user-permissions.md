# ThriveDesk: Get User Permissions



```
GET https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-user-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-user-permissions?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-user-permissions?${params}`, {
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
| `userId` | string | yes | The user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Raw user payload. |
| `email` | string | User email address when returned. |
| `id` | string | User identifier. |
| `name` | string | User name when returned. |
| `role` | string | User role when returned. |

## Native endpoint

Through the native ThriveDesk API, this operation is `GET /v1/settings/users/{{userId}}/permissions` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-permissions.md) for the provider-specific parameters and requirements.

