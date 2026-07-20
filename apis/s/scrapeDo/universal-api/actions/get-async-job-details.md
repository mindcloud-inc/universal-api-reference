# Scrape do: Get async job details

Retrieves async job details from Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-async-job-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-async-job-details?connectionId=$CONNECTION_ID&jobID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-async-job-details?${params}`, {
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
| `jobID` | string | yes | The async job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AcquiredConcurrency": 1,
      "Canceled": true,
      "EndTime": "string",
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
| `Canceled` | boolean | Whether the job was canceled. |
| `EndTime` | string | Job end timestamp. |
| `JobID` | string | Job identifier. |
| `LimitConcurrency` | number | Configured job concurrency limit. |
| `StartTime` | string | Job start timestamp. |
| `Status` | string | Job execution status. |
| `TaskIDs` | array<string> | Task identifiers in the job. |
| `Tasks` | array<object> | Task status records. |

## Native endpoint

Through the native Scrape do API, this operation is `GET https://q.scrape.do/api/v1/jobs/:jobID` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-job-details.md) for the provider-specific parameters and requirements.

