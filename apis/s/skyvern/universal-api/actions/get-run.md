# Skyvern: Get Run

Retrieves task or workflow run details from Skyvern.

```
GET https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/get-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/get-run?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/get-run?${params}`, {
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
| `runId` | string | yes | The task run or workflow run ID. |

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

Through the native Skyvern API, this operation is `GET /v1/runs/:run_id` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-run.md) for the provider-specific parameters and requirements.

