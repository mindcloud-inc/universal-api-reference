# Crowdin: Get Authenticated User

Retrieves the authenticated user from Crowdin.

```
GET https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-authenticated-user?${params}`, {
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
      "avatarUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailVerified": true,
      "fullName": "Ava Chen",
      "id": 1,
      "lastSeen": "2026-05-07T12:00:00.000Z",
      "timezone": "string",
      "twoFactor": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `fullName` | string |  |
| `id` | number |  |
| `lastSeen` | date |  |
| `timezone` | string |  |
| `twoFactor` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Crowdin API, this operation is `GET /user` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

