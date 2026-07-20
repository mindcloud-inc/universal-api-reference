# Pastefy: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pastefy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "auth_type": "string",
      "auth_types": [
        "string"
      ],
      "color": "string",
      "display_name": "Ava Chen",
      "id": "string",
      "logged_in": true,
      "name": "Ava Chen",
      "profile_picture": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth_type` | string | The primary auth type used by the user account. |
| `auth_types` | array<string> | The auth providers enabled for the user account. |
| `color` | string | The profile color value for the current user. |
| `display_name` | string | The display name shown for the current user. |
| `id` | string | The Pastefy user identifier. |
| `logged_in` | boolean | Whether the request is authenticated for the current Pastefy user. |
| `name` | string | The Pastefy username. |
| `profile_picture` | string | The profile picture URL for the current user. |
| `type` | string | The Pastefy account type. |

## Native endpoint

Through the native Pastefy API, this operation is `GET /user` (base URL `https://pastefy.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

