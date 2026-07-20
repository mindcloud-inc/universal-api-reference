# Raindrop: Get Authenticated User



```
GET https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-authenticated-user?${params}`, {
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
      "result": true,
      "user": {
        "_id": 1,
        "avatar": "string",
        "email": "ava@example.com",
        "files": {
          "lastCheckPoint": "string",
          "size": 1,
          "used": 1
        },
        "fullName": "Ava Chen",
        "groups": [
          {}
        ],
        "lastAction": "string",
        "lastUpdate": "string",
        "lastVisit": "string",
        "name": "Ava Chen",
        "password": true,
        "pro": true,
        "registered": "string",
        "tfa": {
          "enabled": true
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |
| `user._id` | number |  |
| `user.avatar` | string |  |
| `user.email` | string |  |
| `user.files.lastCheckPoint` | string |  |
| `user.files.size` | number |  |
| `user.files.used` | number |  |
| `user.fullName` | string |  |
| `user.groups` | array<object> |  |
| `user.lastAction` | string |  |
| `user.lastUpdate` | string |  |
| `user.lastVisit` | string |  |
| `user.name` | string |  |
| `user.password` | boolean |  |
| `user.pro` | boolean |  |
| `user.registered` | string |  |
| `user.tfa.enabled` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `GET /user` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

