# Focusmate: Get Partner Profile

Retrieves a user's public Focusmate profile.

```
GET https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-partner-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Focusmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-partner-profile?connectionId=$CONNECTION_ID&userId=5edcf2e5-539c-4250-966a-468a7ddfa38d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "5edcf2e5-539c-4250-966a-468a7ddfa38d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-partner-profile?${params}`, {
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
| `userId` | string | yes | Focusmate user ID to retrieve public profile data for. Example: `5edcf2e5-539c-4250-966a-468a7ddfa38d`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user": {
        "isFavorite": true,
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
| `user.isFavorite` | boolean | Whether the requested user is currently a favorite partner for the calling user. |
| `user.name` | string | Name of the requested Focusmate user. |
| `user.photoUrl` | string | Profile photo URL when available. |
| `user.timeZone` | string | IANA time zone for the requested user. |
| `user.totalSessionCount` | number | Total number of sessions for the requested user. |
| `user.userId` | string | Unique identifier for the requested Focusmate user. |

## Native endpoint

Through the native Focusmate API, this operation is `GET /users/:userId` (base URL `https://api.focusmate.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-partner-profile.md) for the provider-specific parameters and requirements.

