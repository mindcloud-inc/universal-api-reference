# Florm: Get My Profile

Retrieves your user profile from Florm.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-profile?${params}`, {
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
      "guid": "string",
      "isActive": true,
      "name": "Ava Chen",
      "settings": {
        "language": "string",
        "notificationsEvents": true,
        "notificationsNews": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | User email address. |
| `guid` | string | User GUID. |
| `isActive` | boolean | Whether the user is active. |
| `name` | string | Display name. |
| `settings` | object | User notification and language settings. |
| `settings.language` | string | Preferred language code. |
| `settings.notificationsEvents` | boolean | Whether event notifications are enabled. |
| `settings.notificationsNews` | boolean | Whether news notifications are enabled. |

## Native endpoint

Through the native Florm API, this operation is `GET /v1/auth/me` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-profile.md) for the provider-specific parameters and requirements.

