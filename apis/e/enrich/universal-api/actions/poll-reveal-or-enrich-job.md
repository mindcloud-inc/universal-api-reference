# Enrich.so: Poll Reveal Or Enrich Job

Retrieves reveal or enrich job status from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/poll-reveal-or-enrich-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/poll-reveal-or-enrich-job?connectionId=$CONNECTION_ID&jobId=665a1f4e2c3b7800129dce04" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "665a1f4e2c3b7800129dce04"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/poll-reveal-or-enrich-job?${params}`, {
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
| `jobId` | string | yes | Reveal or enrich job ID. Default: `665a1f4e2c3b7800129dce04`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "jobId": "string",
      "processedItems": 1,
      "progress": 1,
      "status": "string",
      "totalItems": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date | Job completion timestamp. |
| `createdAt` | date | Job creation timestamp. |
| `jobId` | string | Reveal or enrich job identifier. |
| `processedItems` | number | Items processed so far. |
| `progress` | number | Completion percentage from 0 to 100. |
| `status` | string | Current job status. |
| `totalItems` | number | Total items in the job. |
| `type` | string | Reveal or enrich job type. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /lead-finder/reveal-jobs/{jobId}` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/poll-reveal-or-enrich-job.md) for the provider-specific parameters and requirements.

