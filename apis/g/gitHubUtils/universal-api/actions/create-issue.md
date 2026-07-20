# GitHub Utils: Create Issue

Creates a new issue on GitHub.

```
POST https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/create-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "owner": "string",
  "repo": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "owner": "string",
    "repo": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | The issue body. |
| `owner` | string | yes | Repository owner or organization login. |
| `repo` | string | yes | Repository name. |
| `title` | string | yes | The title of the issue. |

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

Through the native GitHub Utils API, this operation is `POST /repos/:owner/:repo/issues` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue.md) for the provider-specific parameters and requirements.

