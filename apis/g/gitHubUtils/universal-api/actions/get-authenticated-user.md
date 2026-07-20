# GitHub Utils: Get Authenticated User

Retrieves the authenticated user from GitHub.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-authenticated-user?${params}`, {
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
      "avatar_url": "https://example.com",
      "bio": "string",
      "blog": "string",
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "followers": 1,
      "following": 1,
      "html_url": "https://example.com",
      "id": 1,
      "location": "string",
      "login": "string",
      "name": "Ava Chen",
      "node_id": "string",
      "public_repos": 1,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_url` | string |  |
| `bio` | string |  |
| `blog` | string |  |
| `company` | string |  |
| `created_at` | date |  |
| `email` | string |  |
| `followers` | number |  |
| `following` | number |  |
| `html_url` | string |  |
| `id` | number |  |
| `location` | string |  |
| `login` | string |  |
| `name` | string |  |
| `node_id` | string |  |
| `public_repos` | number |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /user` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

