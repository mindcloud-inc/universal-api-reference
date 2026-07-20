# Speech is Cheap: Cancel Transcription Job

Deletes a pending transcription job from Speech is Cheap.

```
DELETE https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/cancel-transcription-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speech is Cheap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/cancel-transcription-job?connectionId=$CONNECTION_ID&jobId=00000000-1111-7222-b333-444444444444-sic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "00000000-1111-7222-b333-444444444444-sic"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/cancel-transcription-job?${params}`, {
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
| `jobId` | string | yes | Speech is Cheap transcription job ID to cancel. Example: `00000000-1111-7222-b333-444444444444-sic`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Plain-text cancellation response. Runtime value was OK. |

## Native endpoint

Through the native Speech is Cheap API, this operation is `DELETE /jobs/:job_id` (base URL `https://api.speechischeap.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-transcription-job.md) for the provider-specific parameters and requirements.

