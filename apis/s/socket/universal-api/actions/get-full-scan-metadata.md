# Socket: Get Full Scan Metadata

Retrieves full scan metadata from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-full-scan-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-full-scan-metadata?connectionId=$CONNECTION_ID&fullScanId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fullScanId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-full-scan-metadata?${params}`, {
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
| `fullScanId` | string | yes |  |

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
| `updatedAt` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/full-scans/:full_scan_id/metadata` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-scan-metadata.md) for the provider-specific parameters and requirements.

