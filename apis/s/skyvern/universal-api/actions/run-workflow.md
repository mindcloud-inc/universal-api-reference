# Skyvern: Run Workflow

Runs a workflow in Skyvern.

```
POST https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/run-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/run-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/run-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | string | yes | ID of the workflow to run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiFallback": true,
      "appUrl": "https://example.com",
      "browserProfileId": "string",
      "browserSessionId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "downloadedFiles": [
        {}
      ],
      "errors": [
        {}
      ],
      "failureReason": "string",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "maxScreenshotScrolls": 1,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "output": {},
      "queuedAt": "2026-05-07T12:00:00.000Z",
      "recordingUrl": "https://example.com",
      "runId": "string",
      "runRequest": {},
      "runType": "string",
      "runWith": "string",
      "screenshotUrls": [
        "https://example.com"
      ],
      "scriptRun": {},
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "stepCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiFallback` | boolean | Whether the run can fall back to AI |
| `appUrl` | string | URL to the application UI where the run can be viewed |
| `browserProfileId` | string | ID of the browser profile used for this run |
| `browserSessionId` | string | ID of the persistent browser session used for this run |
| `createdAt` | date | Timestamp when this run was created |
| `downloadedFiles` | array<object> | List of files downloaded during the run |
| `errors` | array<object> | Errors captured for the run |
| `failureReason` | string | Reason for failure if the run failed or terminated |
| `finishedAt` | date | Timestamp when this run finished |
| `maxScreenshotScrolls` | number | Maximum number of screenshot scrolls captured for this run |
| `modifiedAt` | date | Timestamp when this run was last modified |
| `output` | object | Output data from the run, if any |
| `queuedAt` | date | Timestamp when this run was queued |
| `recordingUrl` | string | URL to the recording of the run |
| `runId` | string | Unique identifier for this run |
| `runRequest` | object | Original request parameters used to start this run |
| `runType` | string | Type of run |
| `runWith` | string | Execution mode used for the run |
| `screenshotUrls` | array<string> | List of screenshot URLs |
| `scriptRun` | object | Script run result, when present |
| `startedAt` | date | Timestamp when this run started execution |
| `status` | string | Current status of the run |
| `stepCount` | number | Total number of steps executed in this run |

## Native endpoint

Through the native Skyvern API, this operation is `POST /v1/run/workflows` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-workflow.md) for the provider-specific parameters and requirements.

