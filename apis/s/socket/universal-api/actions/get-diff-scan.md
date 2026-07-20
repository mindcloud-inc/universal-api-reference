# Socket: Get Diff Scan

Retrieves a diff scan from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-diff-scan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-diff-scan?connectionId=$CONNECTION_ID&diffScanId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "diffScanId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-diff-scan?${params}`, {
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
| `diffScanId` | string | yes |  |

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
        "artifacts": {
          "added": [
            {}
          ],
          "removed": [
            {}
          ],
          "replaced": [
            {}
          ],
          "unchanged": [
            {}
          ],
          "updated": [
            {}
          ]
        },
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
      }
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
| `diffScan.artifacts` | object |  |
| `diffScan.artifacts.added` | array<object> |  |
| `diffScan.artifacts.added[]` | object |  |
| `diffScan.artifacts.removed` | array<object> |  |
| `diffScan.artifacts.removed[]` | object |  |
| `diffScan.artifacts.replaced` | array<object> |  |
| `diffScan.artifacts.replaced[]` | object |  |
| `diffScan.artifacts.unchanged` | array<object> |  |
| `diffScan.artifacts.unchanged[]` | object |  |
| `diffScan.artifacts.updated` | array<object> |  |
| `diffScan.artifacts.updated[]` | object |  |
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

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/diff-scans/:diff_scan_id` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-diff-scan.md) for the provider-specific parameters and requirements.

