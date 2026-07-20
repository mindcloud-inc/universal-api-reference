# GitHub Utils: Create Issue Comment

Creates an issue comment on GitHub.

```
POST https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/create-issue-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/create-issue-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "owner": "string",
  "repo": "string",
  "issue_number": 1,
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/create-issue-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "owner": "string",
    "repo": "string",
    "issue_number": 1,
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | string | yes | Repository owner or organization login. |
| `repo` | string | yes | Repository name. |
| `issue_number` | number | yes | Issue number in the repository. |
| `body` | string | yes | The comment body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author_association": "string",
      "body": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "html_url": "https://example.com",
      "id": 1,
      "issue_url": "https://example.com",
      "node_id": "string",
      "reactions": {},
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
| `author_association` | string |  |
| `body` | string |  |
| `created_at` | date |  |
| `html_url` | string |  |
| `id` | number |  |
| `issue_url` | string |  |
| `node_id` | string |  |
| `reactions` | object |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `POST /repos/:owner/:repo/issues/:issue_number/comments` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue-comment.md) for the provider-specific parameters and requirements.

