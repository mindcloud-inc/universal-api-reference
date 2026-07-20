# Socket: List Full Scans

Retrieves organization full scans from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-full-scans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-full-scans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-full-scans?${params}`, {
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
| `branch` | string | no |  |
| `commitHash` | string | no |  |
| `direction` | string | no |  |
| `from` | date | no |  |
| `page` | number | no |  |
| `perPage` | number | no |  |
| `pullRequest` | number | no |  |
| `repo` | string | no |  |
| `sort` | string | no |  |
| `useCursor` | boolean | no |  |
| `workspace` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPage": 1,
      "nextPageCursor": "string",
      "results": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPage` | number |  |
| `nextPageCursor` | string |  |
| `results` | array<object> |  |
| `results[]` | object |  |
| `results[].apiUrl` | string |  |
| `results[].branch` | string |  |
| `results[].commitHash` | string |  |
| `results[].commitMessage` | string |  |
| `results[].committers` | array<string> |  |
| `results[].createdAt` | string |  |
| `results[].htmlReportUrl` | string |  |
| `results[].htmlUrl` | string |  |
| `results[].id` | string |  |
| `results[].integrationBranchUrl` | string |  |
| `results[].integrationCommitUrl` | string |  |
| `results[].integrationPullRequestUrl` | string |  |
| `results[].integrationRepoUrl` | string |  |
| `results[].integrationType` | string |  |
| `results[].organizationId` | string |  |
| `results[].organizationSlug` | string |  |
| `results[].pullRequest` | number |  |
| `results[].repo` | string |  |
| `results[].repositoryId` | string |  |
| `results[].repositorySlug` | string |  |
| `results[].scanState` | string | The current processing status of the SBOM |
| `results[].scanType` | string |  |
| `results[].updatedAt` | string |  |
| `results[].workspace` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/full-scans` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-full-scans.md) for the provider-specific parameters and requirements.

