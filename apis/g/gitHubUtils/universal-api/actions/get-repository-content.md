# GitHub Utils: Get Repository Content

Retrieves repository content from GitHub.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-repository-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-repository-content?connectionId=$CONNECTION_ID&owner=string&repo=string&path=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "owner": "string",
  "repo": "string",
  "path": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-repository-content?${params}`, {
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
| `path` | string | yes | File or directory path in the repository. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "content": "string",
      "download_url": "https://example.com",
      "encoding": "string",
      "git_url": "https://example.com",
      "html_url": "https://example.com",
      "name": "Ava Chen",
      "path": "string",
      "sha": "string",
      "size": 1,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `content` | string |  |
| `download_url` | string |  |
| `encoding` | string |  |
| `git_url` | string |  |
| `html_url` | string |  |
| `name` | string |  |
| `path` | string |  |
| `sha` | string |  |
| `size` | number |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /repos/:owner/:repo/contents/:path` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-repository-content.md) for the provider-specific parameters and requirements.

