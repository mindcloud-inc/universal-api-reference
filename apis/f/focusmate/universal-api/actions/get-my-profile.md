# Focusmate: Get My Profile

Retrieves your personal Focusmate profile data.

```
GET https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-my-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Focusmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-my-profile?${params}`, {
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
      "user": {
        "email": "ava@example.com",
        "memberSince": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "photoUrl": "https://example.com",
        "timeZone": "string",
        "totalSessionCount": 1,
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user.email` | string | Email address for the current Focusmate user. |
| `user.memberSince` | date | Date and time when the user joined Focusmate. |
| `user.name` | string | Name of the current Focusmate user. |
| `user.photoUrl` | string | Profile photo URL for the current user. |
| `user.timeZone` | string | IANA time zone for the current user. |
| `user.totalSessionCount` | number | Total number of sessions for the current user. |
| `user.userId` | string | Unique identifier for the current Focusmate user. |

## Native endpoint

Through the native Focusmate API, this operation is `GET /me` (base URL `https://api.focusmate.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-profile.md) for the provider-specific parameters and requirements.

