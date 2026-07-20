# Dribbble: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dribbble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-current-user?${params}`, {
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
      "bio": "string",
      "canUploadShot": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "followersCount": 1,
      "htmlUrl": "https://example.com",
      "id": 1,
      "links": {},
      "location": "string",
      "login": "string",
      "name": "Ava Chen",
      "pro": true,
      "teams": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `bio` | string |  |
| `canUploadShot` | boolean |  |
| `createdAt` | date |  |
| `email` | string |  |
| `followersCount` | number |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `links` | object |  |
| `location` | string |  |
| `login` | string |  |
| `name` | string |  |
| `pro` | boolean |  |
| `teams` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Dribbble API, this operation is `GET /user` (base URL `https://api.dribbble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

