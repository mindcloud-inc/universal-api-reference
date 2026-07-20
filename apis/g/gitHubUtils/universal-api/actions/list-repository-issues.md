# GitHub Utils: List Repository Issues

Retrieves issues from a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-repository-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-repository-issues?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&repo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "owner": "string",
  "repo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-repository-issues?${params}`, {
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
| `state` | string | no | Issue state to return. |
| `repo` | string | yes | Repository name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {},
      "assignees": [
        {}
      ],
      "author_association": "string",
      "body": "string",
      "closed_at": "2026-05-07T12:00:00.000Z",
      "comments": 1,
      "comments_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "events_url": "https://example.com",
      "html_url": "https://example.com",
      "id": 1,
      "labels": [
        {}
      ],
      "labels_url": "https://example.com",
      "locked": true,
      "milestone": {},
      "node_id": "string",
      "number": 1,
      "repository_url": "https://example.com",
      "state": "string",
      "state_reason": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | object |  |
| `assignees` | array<object> |  |
| `author_association` | string |  |
| `body` | string |  |
| `closed_at` | date |  |
| `comments` | number |  |
| `comments_url` | string |  |
| `created_at` | date |  |
| `events_url` | string |  |
| `html_url` | string |  |
| `id` | number |  |
| `labels` | array<object> |  |
| `labels_url` | string |  |
| `locked` | boolean |  |
| `milestone` | object |  |
| `node_id` | string |  |
| `number` | number |  |
| `repository_url` | string |  |
| `state` | string |  |
| `state_reason` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /repos/:owner/:repo/issues` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-repository-issues.md) for the provider-specific parameters and requirements.

