# Socket: Create Full Scan

Creates a new full scan in Socket.

```
POST https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-full-scan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-full-scan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "repo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-full-scan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "repo": "string"
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
| `committers` | string | no |  |
| `integrationOrgSlug` | string | no |  |
| `integrationType` | string | no | Default: `api`. |
| `makeDefaultBranch` | boolean | no | Default: `false`. |
| `pullRequest` | number | no |  |
| `repo` | string | yes |  |
| `scanType` | string | no | Default: `socket`. |
| `setAsPendingHead` | boolean | no | Default: `false`. |
| `tmp` | boolean | no | Default: `false`. |
| `workspace` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "branch": "string",
      "commitHash": "string",
      "commitMessage": "string",
      "committers": [
        "string"
      ],
      "createdAt": "string",
      "htmlReportUrl": "https://example.com",
      "htmlUrl": "https://example.com",
      "id": "string",
      "integrationBranchUrl": "https://example.com",
      "integrationCommitUrl": "https://example.com",
      "integrationPullRequestUrl": "https://example.com",
      "integrationRepoUrl": "https://example.com",
      "integrationType": "string",
      "organizationId": "string",
      "organizationSlug": "string",
      "pullRequest": 1,
      "repo": "string",
      "repositoryId": "string",
      "repositorySlug": "string",
      "scanState": "string",
      "scanType": "string",
      "unmatchedFiles": [
        "string"
      ],
      "updatedAt": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `branch` | string |  |
| `commitHash` | string |  |
| `commitMessage` | string |  |
| `committers` | array<string> |  |
| `createdAt` | string |  |
| `htmlReportUrl` | string |  |
| `htmlUrl` | string |  |
| `id` | string |  |
| `integrationBranchUrl` | string |  |
| `integrationCommitUrl` | string |  |
| `integrationPullRequestUrl` | string |  |
| `integrationRepoUrl` | string |  |
| `integrationType` | string |  |
| `organizationId` | string |  |
| `organizationSlug` | string |  |
| `pullRequest` | number |  |
| `repo` | string |  |
| `repositoryId` | string |  |
| `repositorySlug` | string |  |
| `scanState` | string | The current processing status of the SBOM |
| `scanType` | string |  |
| `unmatchedFiles` | array<string> |  |
| `updatedAt` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native Socket API, this operation is `POST /orgs/:org_slug/full-scans` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-full-scan.md) for the provider-specific parameters and requirements.

