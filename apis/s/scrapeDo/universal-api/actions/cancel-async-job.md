# Scrape do: Cancel async job

Cancels an async job in Scrape do.

```
DELETE https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/cancel-async-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/cancel-async-job?connectionId=$CONNECTION_ID&jobID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/cancel-async-job?${params}`, {
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
| `jobID` | string | yes | The async job identifier to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AcquiredConcurrency": 1,
      "Canceled": true,
      "Code": 1,
      "EndTime": "string",
      "Error": "string",
      "JobID": "string",
      "LimitConcurrency": 1,
      "StartTime": "string",
      "Status": "string",
      "TaskIDs": [
        "string"
      ],
      "Tasks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AcquiredConcurrency` | number | Concurrency consumed by the job. |
| `Canceled` | boolean | Whether the job is canceled. |
| `Code` | number | Error code when cancellation is not accepted. |
| `EndTime` | string | Job end timestamp. |
| `Error` | string | Error message when cancellation is not accepted. |
| `JobID` | string | Canceled job identifier. |
| `LimitConcurrency` | number | Configured job concurrency limit. |
| `StartTime` | string | Job start timestamp. |
| `Status` | string | Job status after cancel attempt. |
| `TaskIDs` | array<string> | Task identifiers in the job. |
| `Tasks` | array<object> | Task status records. |

## Native endpoint

Through the native Scrape do API, this operation is `DELETE https://q.scrape.do/api/v1/jobs/:jobID` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-async-job.md) for the provider-specific parameters and requirements.

