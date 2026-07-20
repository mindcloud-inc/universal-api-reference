# Dev.to: Get Authenticated User

Retrieves the authenticated Dev.to user.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-authenticated-user?${params}`, {
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
      "id": 1,
      "location": "string",
      "name": "Ava Chen",
      "profile_image": "string",
      "summary": "string",
      "username": "Ava Chen",
      "website_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `location` | string |  |
| `name` | string |  |
| `profile_image` | string |  |
| `summary` | string |  |
| `username` | string |  |
| `website_url` | string |  |

## Native endpoint

Through the native Dev.to API, this operation is `GET /users/me` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

