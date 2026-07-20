# Kickbox: Get Batch Verification Status

Retrieves a batch verification job from Kickbox.

```
GET https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/get-batch-verification-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kickbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/get-batch-verification-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/get-batch-verification-status?${params}`, {
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
| `jobId` | string | yes | The batch verification job ID returned when the batch job was created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "download_url": "https://example.com",
      "duration": 1,
      "error": "string",
      "id": 1,
      "message": "string",
      "name": "Ava Chen",
      "progress": {},
      "stats": {},
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Timestamp when the batch verification job was created. |
| `download_url` | string | Signed CSV download URL when the job has completed. |
| `duration` | number | Batch processing duration in milliseconds. |
| `error` | string | Error details when the batch job fails. |
| `id` | number | Kickbox batch verification job ID. |
| `message` | string | Provider message returned with the job status response. |
| `name` | string | Kickbox-generated batch job name. |
| `progress` | object | In-progress counters returned while Kickbox is processing a batch job. |
| `stats` | object | Summary counts returned for a completed batch verification job. |
| `status` | string | Current job status returned by Kickbox. |
| `success` | boolean | Whether the status request succeeded. |

## Native endpoint

Through the native Kickbox API, this operation is `GET /verify-batch/:jobId` (base URL `https://api.kickbox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-verification-status.md) for the provider-specific parameters and requirements.

