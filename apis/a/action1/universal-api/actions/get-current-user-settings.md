# Action1: Get Current User Settings

Retrieves current user settings from Action1.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-current-user-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-current-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-current-user-settings?${params}`, {
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
      "email": "ava@example.com",
      "emailVerified": "ava@example.com",
      "enabled": "string",
      "firstName": "Ava",
      "id": "string",
      "identityProvider": "string",
      "impersonating": "string",
      "lastName": "Chen",
      "mfa": "string",
      "phone": "string",
      "roles": "string",
      "self": "string",
      "sessionTimeout": 1,
      "system": "string",
      "systemRole": "string",
      "timezone": "string",
      "type": "string",
      "userType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `emailVerified` | string |  |
| `enabled` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `identityProvider` | string |  |
| `impersonating` | string |  |
| `lastName` | string |  |
| `mfa` | string |  |
| `phone` | string |  |
| `roles` | string |  |
| `self` | string |  |
| `sessionTimeout` | number |  |
| `system` | string |  |
| `systemRole` | string |  |
| `timezone` | string |  |
| `type` | string |  |
| `userType` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /me` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-settings.md) for the provider-specific parameters and requirements.

