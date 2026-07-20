# Twist: Get Current User

Retrieves the current authenticated user from Twist.

```
GET https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-current-user?${params}`, {
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
      "avatarUrls": {
        "s195": "https://example.com",
        "s35": "https://example.com",
        "s60": "https://example.com",
        "s640": "https://example.com"
      },
      "bot": true,
      "clientId": "string",
      "dateFormat": "string",
      "defaultWorkspace": 1,
      "email": "ava@example.com",
      "emails": [
        {
          "email": "ava@example.com",
          "primary": true
        }
      ],
      "featureIdentifier": "string",
      "firstName": "Ava",
      "id": 1,
      "lang": "string",
      "name": "Ava Chen",
      "removed": true,
      "restricted": true,
      "scheduledBanners": [
        "string"
      ],
      "setupPending": true,
      "shortName": "Ava Chen",
      "snoozed": true,
      "theme": "string",
      "timeFormat": "string",
      "timezone": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrls.s195` | string |  |
| `avatarUrls.s35` | string |  |
| `avatarUrls.s60` | string |  |
| `avatarUrls.s640` | string |  |
| `bot` | boolean |  |
| `clientId` | string |  |
| `dateFormat` | string |  |
| `defaultWorkspace` | number |  |
| `email` | string |  |
| `emails[].email` | string |  |
| `emails[].primary` | boolean |  |
| `featureIdentifier` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lang` | string |  |
| `name` | string |  |
| `removed` | boolean |  |
| `restricted` | boolean |  |
| `scheduledBanners[]` | string |  |
| `setupPending` | boolean |  |
| `shortName` | string |  |
| `snoozed` | boolean |  |
| `theme` | string |  |
| `timeFormat` | string |  |
| `timezone` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Twist API, this operation is `GET /users/get_session_user` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

