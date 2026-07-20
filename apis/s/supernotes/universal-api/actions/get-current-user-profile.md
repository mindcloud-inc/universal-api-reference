# Supernotes: Get Current User Profile

Retrieves the authenticated user profile from Supernotes.

```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-current-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-current-user-profile?${params}`, {
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
      "bio": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "photo": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bio` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `photo` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /profiles` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-profile.md) for the provider-specific parameters and requirements.

