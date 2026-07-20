# StoryChief: Get Current User

Retrieves the current user from StoryChief.

```
GET https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a StoryChief `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/get-current-user?${params}`, {
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
      "account": {
        "data": {
          "id": 1,
          "name": "Ava Chen"
        }
      },
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": 1,
      "lastname": "Chen",
      "phone": "string",
      "profilePicture": {
        "data": {
          "alt": "string",
          "name": "Ava Chen",
          "sizes": {
            "full": "string",
            "large": "string",
            "regular": "string"
          },
          "url": "https://example.com"
        }
      },
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.data.id` | number |  |
| `account.data.name` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `lastname` | string |  |
| `phone` | string |  |
| `profilePicture.data.alt` | string |  |
| `profilePicture.data.name` | string |  |
| `profilePicture.data.sizes.full` | string |  |
| `profilePicture.data.sizes.large` | string |  |
| `profilePicture.data.sizes.regular` | string |  |
| `profilePicture.data.url` | string |  |
| `role` | string |  |

## Native endpoint

Through the native StoryChief API, this operation is `GET /me` (base URL `https://api.storychief.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

