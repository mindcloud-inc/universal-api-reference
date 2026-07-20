# GitHub Utils: List Pull Request Files

Retrieves files from a GitHub pull request.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-pull-request-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-pull-request-files?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&repo=string&pull_number=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "owner": "string",
  "repo": "string",
  "pull_number": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-pull-request-files?${params}`, {
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
| `pull_number` | number | yes | Pull request number in the repository. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additions": 1,
      "blob_url": "https://example.com",
      "changes": 1,
      "contents_url": "https://example.com",
      "deletions": 1,
      "filename": "Ava Chen",
      "patch": "string",
      "raw_url": "https://example.com",
      "sha": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additions` | number |  |
| `blob_url` | string |  |
| `changes` | number |  |
| `contents_url` | string |  |
| `deletions` | number |  |
| `filename` | string |  |
| `patch` | string |  |
| `raw_url` | string |  |
| `sha` | string |  |
| `status` | string |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /repos/:owner/:repo/pulls/:pull_number/files` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pull-request-files.md) for the provider-specific parameters and requirements.

