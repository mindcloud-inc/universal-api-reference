# Google Slides: Get Current User

Retrieves the profile of the Google account that authorized the connection.

```
GET https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-current-user?${params}`, {
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
      "name": "Ava Chen",
      "email": "ava@example.com",
      "givenName": "Ava",
      "familyName": "Chen",
      "hd": "Ava Chen",
      "emailVerified": true,
      "sub": "string",
      "picture": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | The user's full display name. |
| `email` | string | The user's email address. |
| `givenName` | string | The user's given name. |
| `familyName` | string | The user's family name. |
| `hd` | string | The Google Workspace domain of the account, when it belongs to one. |
| `emailVerified` | boolean | Whether Google has verified the email address. |
| `sub` | string | The unique Google account identifier of the user. |
| `picture` | string | The URL of the user's profile picture. |

## Native endpoint

Through the native Google Slides API, this operation is `GET /v1/userinfo` (base URL `https://openidconnect.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

