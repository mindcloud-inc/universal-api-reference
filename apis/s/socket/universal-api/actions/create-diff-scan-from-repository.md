# Socket: Create Diff Scan from Repository

Creates a diff scan in Socket from a repository.

```
POST https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-diff-scan-from-repository
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-diff-scan-from-repository" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "repoSlug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-diff-scan-from-repository', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "repoSlug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branch` | string | no |  |
| `commitHash` | string | no |  |
| `commitMessage` | string | no |  |
| `committers` | list<string> | no |  |
| `description` | string | no |  |
| `externalHref` | string | no |  |
| `integrationOrgSlug` | string | no |  |
| `integrationType` | string | no |  |
| `merge` | boolean | no |  |
| `pullRequest` | number | no |  |
| `workspace` | string | no |  |
| `repoSlug` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "diffScan": {
        "afterFullScan": {
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
        "apiUrl": "https://example.com",
        "beforeFullScan": {
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
        "createdAt": "string",
        "description": "string",
        "externalHref": "string",
        "htmlUrl": "https://example.com",
        "id": "string",
        "merge": true,
        "organizationId": "string",
        "repositoryId": "string",
        "updatedAt": "string"
      },
      "unmatchedAfterFiles": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `diffScan` | object |  |
| `diffScan.afterFullScan` | object |  |
| `diffScan.afterFullScan.apiUrl` | string |  |
| `diffScan.afterFullScan.branch` | string |  |
| `diffScan.afterFullScan.commitHash` | string |  |
| `diffScan.afterFullScan.commitMessage` | string |  |
| `diffScan.afterFullScan.committers` | array<string> |  |
| `diffScan.afterFullScan.createdAt` | string |  |
| `diffScan.afterFullScan.htmlUrl` | string |  |
| `diffScan.afterFullScan.id` | string |  |
| `diffScan.afterFullScan.organizationId` | string |  |
| `diffScan.afterFullScan.organizationSlug` | string |  |
| `diffScan.afterFullScan.pullRequest` | number |  |
| `diffScan.afterFullScan.repositoryId` | string |  |
| `diffScan.afterFullScan.repositorySlug` | string |  |
| `diffScan.afterFullScan.updatedAt` | string |  |
| `diffScan.apiUrl` | string |  |
| `diffScan.beforeFullScan` | object |  |
| `diffScan.beforeFullScan.apiUrl` | string |  |
| `diffScan.beforeFullScan.branch` | string |  |
| `diffScan.beforeFullScan.commitHash` | string |  |
| `diffScan.beforeFullScan.commitMessage` | string |  |
| `diffScan.beforeFullScan.committers` | array<string> |  |
| `diffScan.beforeFullScan.createdAt` | string |  |
| `diffScan.beforeFullScan.htmlUrl` | string |  |
| `diffScan.beforeFullScan.id` | string |  |
| `diffScan.beforeFullScan.organizationId` | string |  |
| `diffScan.beforeFullScan.organizationSlug` | string |  |
| `diffScan.beforeFullScan.pullRequest` | number |  |
| `diffScan.beforeFullScan.repositoryId` | string |  |
| `diffScan.beforeFullScan.repositorySlug` | string |  |
| `diffScan.beforeFullScan.updatedAt` | string |  |
| `diffScan.createdAt` | string |  |
| `diffScan.description` | string |  |
| `diffScan.externalHref` | string |  |
| `diffScan.htmlUrl` | string |  |
| `diffScan.id` | string |  |
| `diffScan.merge` | boolean |  |
| `diffScan.organizationId` | string |  |
| `diffScan.repositoryId` | string |  |
| `diffScan.updatedAt` | string |  |
| `unmatchedAfterFiles` | array<string> |  |

## Native endpoint

Through the native Socket API, this operation is `POST /orgs/:org_slug/diff-scans/from-repo/:repo_slug` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-diff-scan-from-repository.md) for the provider-specific parameters and requirements.

