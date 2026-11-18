# GitHub: Search Pull Request States



```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/search-pull-request-states
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/search-pull-request-states?connectionId=$CONNECTION_ID&searchQuery=is%3Apr%20is%3Aopen%20author%3A%40me%20archived%3Afalse" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchQuery": "is:pr is:open author:@me archived:false"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/search-pull-request-states?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `searchQuery` | string | yes | GitHub search qualifiers, for example: is:pr is:open author:@me archived:false Example: `is:pr is:open author:@me archived:false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `POST /graphql` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-pull-request-states.md) for the provider-specific parameters and requirements.

