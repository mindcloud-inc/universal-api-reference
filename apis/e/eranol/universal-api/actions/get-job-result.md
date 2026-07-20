# Eranol: Get Job Result

Retrieves the result of an Eranol job.

```
GET https://connect.mindcloud.co/v1/universal/eranol/latest/actions/get-job-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eranol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eranol/latest/actions/get-job-result?connectionId=$CONNECTION_ID&job_id=460719d5-d0ad-4fd8-a81c-ebc2435fbfaa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "job_id": "460719d5-d0ad-4fd8-a81c-ebc2435fbfaa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eranol/latest/actions/get-job-result?${params}`, {
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
| `job_id` | string | yes | Job ID returned by an Eranol create action. Example: `460719d5-d0ad-4fd8-a81c-ebc2435fbfaa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "filename": "Ava Chen",
      "format": "string",
      "jobId": "string",
      "jobType": "string",
      "resolution": "string",
      "url": "https://example.com",
      "videoCodec": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number | Result media duration in seconds. |
| `filename` | string | Result file name. |
| `format` | string | Result media format. |
| `jobId` | string | Unique Eranol job identifier. |
| `jobType` | string | Provider job type label. |
| `resolution` | string | Result media resolution. |
| `url` | string | Result file URL. |
| `videoCodec` | string | Result video codec when available. |

## Native endpoint

Through the native Eranol API, this operation is `GET /ffmpeg/result/:job_id` (base URL `https://eranol.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-result.md) for the provider-specific parameters and requirements.

