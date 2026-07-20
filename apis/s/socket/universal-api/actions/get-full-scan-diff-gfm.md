# Socket: Get Full Scan Diff GFM

Retrieves a full scan diff as GitHub Flavored Markdown from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-full-scan-diff-gfm
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-full-scan-diff-gfm?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-full-scan-diff-gfm?${params}`, {
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
      "after": {
        "apiUrl": "https://example.com",
        "branch": "string",
        "commitHash": "string",
        "commitMessage": "string",
        "committers": [
          "string"
        ],
        "createdAt": "string",
        "htmlUrl": "https://example.com",
        "id": "string",
        "organizationId": "string",
        "organizationSlug": "string",
        "pullRequest": 1,
        "repositoryId": "string",
        "repositorySlug": "string",
        "updatedAt": "string"
      },
      "before": {
        "apiUrl": "https://example.com",
        "branch": "string",
        "commitHash": "string",
        "commitMessage": "string",
        "committers": [
          "string"
        ],
        "createdAt": "string",
        "htmlUrl": "https://example.com",
        "id": "string",
        "organizationId": "string",
        "organizationSlug": "string",
        "pullRequest": 1,
        "repositoryId": "string",
        "repositorySlug": "string",
        "updatedAt": "string"
      },
      "comments": {
        "alerts": "string",
        "overview": "string"
      },
      "diffReportUrl": "https://example.com",
      "directDependenciesChanged": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `after` | object |  |
| `after.apiUrl` | string |  |
| `after.branch` | string |  |
| `after.commitHash` | string |  |
| `after.commitMessage` | string |  |
| `after.committers` | array<string> |  |
| `after.createdAt` | string |  |
| `after.htmlUrl` | string |  |
| `after.id` | string |  |
| `after.organizationId` | string |  |
| `after.organizationSlug` | string |  |
| `after.pullRequest` | number |  |
| `after.repositoryId` | string |  |
| `after.repositorySlug` | string |  |
| `after.updatedAt` | string |  |
| `before` | object |  |
| `before.apiUrl` | string |  |
| `before.branch` | string |  |
| `before.commitHash` | string |  |
| `before.commitMessage` | string |  |
| `before.committers` | array<string> |  |
| `before.createdAt` | string |  |
| `before.htmlUrl` | string |  |
| `before.id` | string |  |
| `before.organizationId` | string |  |
| `before.organizationSlug` | string |  |
| `before.pullRequest` | number |  |
| `before.repositoryId` | string |  |
| `before.repositorySlug` | string |  |
| `before.updatedAt` | string |  |
| `comments` | object |  |
| `comments.alerts` | string |  |
| `comments.overview` | string |  |
| `diffReportUrl` | string |  |
| `directDependenciesChanged` | boolean |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/full-scans/diff/gfm` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-scan-diff-gfm.md) for the provider-specific parameters and requirements.

