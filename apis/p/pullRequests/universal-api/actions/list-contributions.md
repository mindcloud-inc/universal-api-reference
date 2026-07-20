# 24 Pull Requests: List Contributions

Retrieves contributions from 24 Pull Requests.

```
GET https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/list-contributions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 24 Pull Requests `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/list-contributions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/list-contributions?${params}`, {
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
      "body": "string",
      "issue_url": "https://example.com",
      "repo_name": "Ava Chen",
      "title": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string | Contribution body text. |
| `issue_url` | string | Issue or pull request URL. |
| `repo_name` | string | Repository name. |
| `title` | string | Contribution title. |
| `user` | object | User who made the contribution. |

## Native endpoint

Through the native 24 Pull Requests API, this operation is `GET /pull_requests.json` (base URL `https://24pullrequests.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contributions.md) for the provider-specific parameters and requirements.

