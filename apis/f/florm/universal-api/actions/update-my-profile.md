# Florm: Update My Profile

Updates your user profile in Florm.

```
PUT https://connect.mindcloud.co/v1/universal/florm/latest/actions/update-my-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/florm/latest/actions/update-my-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "name": "Ava Chen",
  "settings.notificationsNews": true,
  "settings.notificationsEvents": true,
  "settings.language": "ru"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/florm/latest/actions/update-my-profile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "name": "Ava Chen",
    "settings.notificationsNews": true,
    "settings.notificationsEvents": true,
    "settings.language": "ru"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address for the Florm profile. |
| `name` | string | yes | Display name for the Florm profile. |
| `settings.notificationsNews` | boolean | yes | Whether to receive Florm news notifications. |
| `settings.notificationsEvents` | boolean | yes | Whether to receive Florm event notifications. |
| `settings.language` | string | yes | Language code for the Florm profile. Default: `ru`. |

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
      "settings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address on the updated Florm profile. |
| `guid` | string | GUID of the updated Florm user. |
| `isActive` | boolean | Whether the updated user is active. |
| `name` | string | Updated display name. |
| `settings` | object | Updated user settings. |

## Native endpoint

Through the native Florm API, this operation is `PUT /v1/auth/me` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-my-profile.md) for the provider-specific parameters and requirements.

