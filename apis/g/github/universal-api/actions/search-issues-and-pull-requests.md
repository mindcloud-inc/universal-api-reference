# GitHub: Search Issues and Pull Requests

Finds GitHub issues and pull requests by search query.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/search-issues-and-pull-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/search-issues-and-pull-requests?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/search-issues-and-pull-requests?${params}`, {
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
| `q` | string | yes | GitHub search query, for example "is:pr is:open review-requested:@me". Include is:issue or is:pr. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `advanced_search` | string | no | Set true to opt into advanced search syntax when needed. |
| `per_page` | number | no | The number of results per page (max 100). Default: `50`. |
| `sort` | string | no | Sort field: created, updated or comments. Default is best match. One of: `0`, `1`, `2`. |
| `order` | string | no | Sort direction: asc or desc. Default is desc. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "draft": true,
      "htmlUrl": "https://example.com",
      "labels": [
        {
          "color": "string",
          "name": "Ava Chen"
        }
      ],
      "number": 1,
      "pullRequest": {
        "htmlUrl": "https://example.com"
      },
      "repositoryUrl": "https://example.com",
      "state": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "avatarUrl": "https://example.com",
        "login": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `draft` | boolean |  |
| `htmlUrl` | string |  |
| `labels[].color` | string |  |
| `labels[].name` | string |  |
| `number` | number |  |
| `pullRequest.htmlUrl` | string |  |
| `repositoryUrl` | string |  |
| `state` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `user.avatarUrl` | string |  |
| `user.login` | string |  |

## Native endpoint

Through the native GitHub API, this operation is `GET /search/issues` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-issues-and-pull-requests.md) for the provider-specific parameters and requirements.

