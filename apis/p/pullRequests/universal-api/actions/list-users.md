# 24 Pull Requests: List Users

Retrieves users from 24 Pull Requests.

```
GET https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 24 Pull Requests `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/list-users?${params}`, {
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
      "contributions_count": 1,
      "github_profile": "https://example.com",
      "gravatar_id": "string",
      "id": 1,
      "link": "https://example.com",
      "nickname": "Ava Chen",
      "organisations": [
        {}
      ],
      "pull_requests": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contributions_count` | number | Contribution count. |
| `github_profile` | string | GitHub profile URL. |
| `gravatar_id` | string | Gravatar identifier. |
| `id` | number | 24 Pull Requests user ID. |
| `link` | string | 24 Pull Requests user page. |
| `nickname` | string | User nickname. |
| `organisations` | array<object> | Organisations for the user. |
| `pull_requests` | array<object> | User contributions. |

## Native endpoint

Through the native 24 Pull Requests API, this operation is `GET /users.json` (base URL `https://24pullrequests.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

