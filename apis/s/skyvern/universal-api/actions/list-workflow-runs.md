# Skyvern: List Workflow Runs

Retrieves workflow runs for your organization from Skyvern.

```
GET https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-workflow-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-workflow-runs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-workflow-runs?${params}`, {
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
| `errorCode` | string | no | Exact-match filter on task error_code values. |
| `searchKey` | string | no | Case-insensitive substring search across run metadata. |
| `status` | string | no | Filter by one or more run statuses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiFallback": true,
      "browserAddress": "string",
      "browserProfileId": "string",
      "browserSessionId": "string",
      "codeGen": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "debugSessionId": "string",
      "dependsOnWorkflowRunId": "string",
      "extraHttpHeaders": {},
      "failureReason": "string",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "jobId": "string",
      "maxScreenshotScrolls": 1,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "organizationId": "string",
      "parentWorkflowRunId": "string",
      "proxyLocation": {},
      "queuedAt": "2026-05-07T12:00:00.000Z",
      "runWith": "string",
      "scriptRun": {},
      "sequentialKey": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "totpIdentifier": "string",
      "totpVerificationUrl": "https://example.com",
      "webhookCallbackUrl": "https://example.com",
      "webhookFailureReason": "string",
      "workflowId": "string",
      "workflowPermanentId": "string",
      "workflowRunId": "string",
      "workflowTitle": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiFallback` | boolean | Whether the run can fall back to AI |
| `browserAddress` | string | Browser address used for the workflow run |
| `browserProfileId` | string | Browser profile ID |
| `browserSessionId` | string | Browser session ID |
| `codeGen` | boolean | Whether code generation was used |
| `createdAt` | date | Workflow run creation timestamp |
| `debugSessionId` | string | Debug session ID |
| `dependsOnWorkflowRunId` | string | Workflow run dependency ID |
| `extraHttpHeaders` | object | Additional HTTP headers used during the run |
| `failureReason` | string | Failure reason for the workflow run |
| `finishedAt` | date | Time when the workflow run finished |
| `jobId` | string | Associated job ID |
| `maxScreenshotScrolls` | number | Maximum number of screenshot scrolls |
| `modifiedAt` | date | Workflow run last modification timestamp |
| `organizationId` | string | Organization ID |
| `parentWorkflowRunId` | string | Parent workflow run ID |
| `proxyLocation` | object | Proxy location configuration |
| `queuedAt` | date | Time when the workflow run was queued |
| `runWith` | string | Execution mode used for the workflow run |
| `scriptRun` | object | Script run result, when present |
| `sequentialKey` | string | Sequential execution key |
| `startedAt` | date | Time when the workflow run started |
| `status` | string | Workflow run status |
| `totpIdentifier` | string | TOTP identifier |
| `totpVerificationUrl` | string | TOTP verification URL |
| `webhookCallbackUrl` | string | Webhook callback URL |
| `webhookFailureReason` | string | Webhook failure reason |
| `workflowId` | string | Workflow ID |
| `workflowPermanentId` | string | Permanent workflow identifier |
| `workflowRunId` | string | Workflow run ID |
| `workflowTitle` | string | Workflow title |

## Native endpoint

Through the native Skyvern API, this operation is `GET /v1/workflows/runs` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflow-runs.md) for the provider-specific parameters and requirements.

