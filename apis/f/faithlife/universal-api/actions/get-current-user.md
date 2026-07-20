# Faithlife: Get Current User

Retrieves the current user from Faithlife.

```
GET https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faithlife `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/get-current-user?${params}`, {
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
      "alias": "string",
      "avatarUrls": {},
      "dayPhone": "string",
      "email": "ava@example.com",
      "gender": "string",
      "id": "string",
      "isSolicitable": true,
      "name": "Ava Chen",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `avatarUrls` | object |  |
| `dayPhone` | string |  |
| `email` | string |  |
| `gender` | string |  |
| `id` | string |  |
| `isSolicitable` | boolean |  |
| `name` | string |  |
| `token` | string |  |

## Native endpoint

Through the native Faithlife API, this operation is `GET /users/me` (base URL `https://accountsapi.logos.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

