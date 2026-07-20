# Murf Dub: Get Dubbing Job Status

Retrieves a Murf Dub job status.

```
GET https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/get-dubbing-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Murf Dub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/get-dubbing-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/get-dubbing-job-status?${params}`, {
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
| `jobId` | string | yes | The Murf Dub job ID to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_remaining": 1,
      "credits_used": 1,
      "download_details": [
        {
          "download_srt_url": "https://example.com",
          "download_url": "https://example.com",
          "error_message": "string",
          "locale": "string",
          "status": "string"
        }
      ],
      "failure_code": "string",
      "failure_reason": "string",
      "job_id": "string",
      "project_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number | Remaining credits after the job update. |
| `credits_used` | number | Credits consumed by the job. |
| `download_details[].download_srt_url` | string | Subtitle download URL for the locale. |
| `download_details[].download_url` | string | Rendered media download URL for the locale. |
| `download_details[].error_message` | string | Per-locale failure message when present. |
| `download_details[].locale` | string | Locale for one output artifact. |
| `download_details[].status` | string | Per-locale output status. |
| `failure_code` | string | Top-level provider failure code when the job fails. |
| `failure_reason` | string | Top-level provider failure reason when the job fails. |
| `job_id` | string | Murf job identifier. |
| `project_id` | string | Project ID associated with the dubbing job. |
| `status` | string | Current Murf processing status for the job. |

## Native endpoint

Through the native Murf Dub API, this operation is `GET /v1/murfdub/jobs/:job_id/status` (base URL `https://api.murf.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dubbing-job-status.md) for the provider-specific parameters and requirements.

