# GitHub: Get Issue

Retrieves an issue from a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/get-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/get-issue?connectionId=$CONNECTION_ID&owner=string&repo=string&issue_number=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "owner": "string",
  "repo": "string",
  "issue_number": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/get-issue?${params}`, {
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
| `owner` | string | yes | Repository owner or organization login. |
| `repo` | string | yes | Repository name. |
| `issue_number` | number | yes | Issue number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `GET /repos/:owner/:repo/issues/:issue_number` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue.md) for the provider-specific parameters and requirements.

