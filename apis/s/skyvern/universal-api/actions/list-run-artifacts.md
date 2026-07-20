# Skyvern: List Run Artifacts

Retrieves artifacts for a run from Skyvern.

```
GET https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-run-artifacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-run-artifacts?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-run-artifacts?${params}`, {
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
| `artifactType` | string | no | Optional filter for artifacts returned by the run. |
| `runId` | string | yes | The task run or workflow run ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiSuggestionId": "string",
      "artifactId": "string",
      "artifactType": "string",
      "bundleKey": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "observerCruiseId": "string",
      "observerThoughtId": "string",
      "organizationId": "string",
      "runId": "string",
      "signedUrl": "https://example.com",
      "stepId": "string",
      "taskId": "string",
      "uri": "string",
      "workflowRunBlockId": "string",
      "workflowRunId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiSuggestionId` | string | AI suggestion ID |
| `artifactId` | string | Artifact ID |
| `artifactType` | string | Artifact type |
| `bundleKey` | string | Artifact bundle key |
| `createdAt` | date | Artifact creation timestamp |
| `modifiedAt` | date | Artifact last modification timestamp |
| `observerCruiseId` | string | Observer cruise ID |
| `observerThoughtId` | string | Observer thought ID |
| `organizationId` | string | Organization ID |
| `runId` | string | Run ID |
| `signedUrl` | string | Signed URL for downloading the artifact |
| `stepId` | string | Step ID |
| `taskId` | string | Task ID |
| `uri` | string | Artifact storage URI |
| `workflowRunBlockId` | string | Workflow run block ID |
| `workflowRunId` | string | Workflow run ID |

## Native endpoint

Through the native Skyvern API, this operation is `GET /v1/runs/:run_id/artifacts` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-run-artifacts.md) for the provider-specific parameters and requirements.

