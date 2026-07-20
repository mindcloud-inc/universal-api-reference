# Gumroad: Get User

Retrieves the current user from Gumroad.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-user?${params}`, {
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
      "success": true,
      "user": {
        "bio": "string",
        "currencyType": "string",
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "id": "string",
        "links": [
          [
            "https://example.com"
          ]
        ],
        "name": "Ava Chen",
        "profileUrl": "https://example.com",
        "twitterHandle": "string",
        "url": "https://example.com",
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
| `success` | boolean |  |
| `user` | object |  |
| `user.bio` | string |  |
| `user.currencyType` | string |  |
| `user.displayName` | string |  |
| `user.email` | string |  |
| `user.id` | string |  |
| `user.links[]` | array<string> |  |
| `user.name` | string |  |
| `user.profileUrl` | string |  |
| `user.twitterHandle` | string |  |
| `user.url` | string |  |
| `user.userId` | string |  |

## Native endpoint

Through the native Gumroad API, this operation is `GET /user` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

